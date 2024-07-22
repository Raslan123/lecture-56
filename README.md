# lecture-56
#include <iostream>
using namespace std;
class node{
    public:
    int data;
    node* next;
    node(int dataa){
        this->data=dataa;
        this->next=NULL;
    }
};
void printnode(node * &node){
    cout<<"Value " <<node->data<<endl;
    cout<<"Address "<<node->next;
}
int main(){
    node * node1 = new node(3);
     node * node2 = new node(5);
      node * node3 = new node(7);
      node1->next = node2;
      node2->next = node3;
    printnode(node1);
    printnode(node1->next);
    printnode(node1->next->next);
    return 0;

}
