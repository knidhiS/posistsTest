# posistsTest
#include <stdio.h>
void LCUtil(Node* root, int cl,int expected, int &res)
{
    if (root == NULL)
        return;
 
  
    if (root->data == expected)
        cl++;
    else
        cl = 1;
 
   
    res = max(res, cl);
 
   
    LCU(root->left,cl,root->data + 1, res);
    LCU(root->right,cl,root->data + 1, res);
}
int longest(Node* root)
{
    if (root == NULL)
        return 0;
 
    int res = 0;
 
   LCU(root, 0, root->data, res);
 
    return res;
}


int EDncrypt()
{
   int option,value;
   printf("\nPlease choose following options:\n");
   printf("1 = Encrypt the data.\n");
   printf("2 = Decrypt the data.\n");
   scanf("%d", &option);
   value=data;
   switch(option)
   {
   case 1:
        value = value + 3; 
        return value;
        break;

   case 2:
        value = value - 3; 
        return value;
        break;

   default:
      printf("\nError\n");
   }
   return 0;
}


struct node 
{
    int data;
    struct node *left;
    struct node *right;

};
int newNode(){
	int val;
	printf("value of the node");
	gets(val);  
	//scanf("%d",&val);

  	struct node *root = newNode(val);
	return (node); 

} 
int subNode(){
  int val;
  printf("value of the left node");
  gets(val);
  root->left = newNode(val);
  
  printf("value of the right node");
  gets(val);
  root->right       = newNode(val);

  printf("value of the left most node");
  gets(val);
  int x <= root-((root->left)+(root->right))
  if(val == x ){
  root->left->left  = newNode(val);
 
  }
  else{
   printf("value must be less than %d ",x);
  }

  return (node); 
}
struct node* newNode(int data)
{
  struct node* node = (struct node*)malloc(sizeof(struct node));
  encrypt(data);
  node->data = data;
  node->left = NULL;
  node->right = NULL;
  return(node);
}

int search(int x, Node* root){
	int val=x;
        int flag;
	if (root == NULL)
        return 0;
        
        for(int i=0;node != Null;i++){
}
}
 
 
 
 
int main()
{
  int option,res;
  printf("\nPlease choose following options:\n");

  printf("1 = create the root node.\n");
  printf("2 = create the set of child node.\n");
  printf("4 = for encryting/decrypting the data.\n");
  printf("8 = longest chain of genesis node.\n");
  printf("9 = longst chain of any node.\n");
  scanf("%d",&option);
  switch(option){
	case 1 :
		newNode();
		break;  

	case 2 :
		subNode();
		break;  
	case 4 :
		EDncrypt();
		break; 

	case 8 :
		longest(root);
		printf("longest length from Genesis node is %d",res);
		break; 
	case 9 :
		printf("node from which you wanna find the length");
		int x;
		search(x, root);
		printf("longest length from  node is %d",res);
		break; 
	default :
		printf("wrong input ...compile again"); 
 
 }
  return 0;
}
