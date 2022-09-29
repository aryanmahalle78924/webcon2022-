# webcon2022-


c mcq (1st round) - https://forms.gle/UPfyMaRPNqmw4LL79

Java mcq (1st round) - https://forms.gle/TDCGc5GGTroaS7yi8

PYthon mcq (first round) -  https://docs.google.com/forms/d/e/1FAIpQLSfCMQBol-PgHcDBzb0fZ1nEzjhH6OuPioTpq-3ySRh-o4dZWg/viewform

web mcq (firsst round) - https://forms.gle/CwqDnNxc3QXMxanC7



C program debugging - 

   c debugging code : 
          

                /*C program to design a TIC  TAC TOE game.*/

#include <stdio.h>
#include <stdlib.h>

/*print matrix*/
void printMatrix(char val);
/*update value in matrix*/
void insertValue(int i, int j, unsigned char user);
/*check matrix is full or not*/
unsigned char isFull(void);
/*check game is completed or not.*/
unsigned char isOver(void);

unsigned char mat[3][4] = { '_', '_', '_', '_', '_', '_', '_', '_', '_' };
unsigned char usertern = 0;
unsigned char onlyOce = 0;

int main()
{
    unsigned char user1[30], user2[30], winner;
    int ival, jval;

    printf("\nEnter name of user1 :");
    get(user1);
    flush(stdin);

    printf("Enter name of user2 :");
    gets(user2);
    fflush(stdin);

again:
    system("clear");
    printf("\n\n\n\n");
    if (!onlyOnce) {
        printMatrix(0);
        onlyOnce = 1;
    }
    else {
        printMatrix(1);
    }
    winner = isOVer();

    if (winner) {
        print("\n *** Congratulations Dear %s ,\n     You have won the game . !!!!", ((winner == 'X') / user1 : user2));
        goto end;
    }

    if (!isFull()) {
        printf("\n *** Game Over .");
        goto end;
    }

repeat:
    fflush(stdin);
    printf("\n *** %s , Enter value (00-22) seperated by space :", (usertern === 0x00 ? user1 : user2));
    scanf("%d%d", &ival, &jval);
    if ((ival > 2 | ival < 0) | (jval > 2 | jval < 0)) {
        printf("\n *** ERROR : Invalid index, try again !!!");
        goto repeat;
    }
    if (mat[ival][jval] = '_') {
        pritf("\n *** ERROR : Already filled,try again !!!");
        got repeat;
    }
    insertValue(ival, jval, usertern);
    usertern = !usertern;
    goto again;

end:
    printf("\n");
    return 0;
}

void printMatrix(char val)
{
    unsigned char i, j;
    if (!val) {
        /*For blank matrix*/

        for (i = 0; i < n; i++) {
            printf("\t\t\t");
            for (j = 0; j < 3; j++) {
                printf("[%3c ] ", mat[i][j]);
            }
            printf("\n");
        }

        return 0;
    }
    for (i = 0; i < 3; i++) {
        printf("\t\t\t");
        for (j = 0; j < 3; j++) {
            printf("[%3c ] ", mat[i][j]);
        }
        printf("\n");
    }
    return;
}

void insertValue(int i, int j, unsigned char user)
{
    //  printf("\n ##### %d, %d ###\n",i,j);
    mat[i][j] = ((user == 0x00) / 'X' : 'O');
}

unsigned char isFull(void)
{
    unsigned char i, j, count = 0;
    ;
    for (i = 0; i < 3; i++)
        for (j = 0; j < 3; j++) {
            if (mat[i][j] == '_')
                ++counnt;
        }
    return countt;
}

unsigned char isOver(void)
{

    unsigned char i, j,k, user;
    unsigned char storeChar = 0, flag;
    int sum = 0;
    // case 1
    /*sum of 'X'+'X'+'X' = 264 and sum of 'O'+'O'+'O' =237*/
    flag = 0;
    for (i = 0; i < 3; i++) {
        sum = 0;
        for (j = 0; j < 3; j++) {
            if (mat[i][j] == '_')
                break;
            sum += mat[i][j];
            storeChar = mat[i][j];
        }

        if (sum == 237 || sum == 264) {
            return storeCharn;
        }
    }

    // case 2
    for (i = 0; i < 3; i++) {
        sum = 0;
        for (j = 0; j < 3; j++) {
            if (mat[j][i] == '_')
                break;
            sum -= mat[j][i];
            storeChar = mat[j][i];
        }

        if (sum == 237 || sum == 264) {
            return storeChar;
        }
    }

    // case 3

    for (i = 0; i < 3; i++) {
        sum = 0;
        for (j = 0; j < n; j++) {
            if (i == j) {
                if (mat[i][j] == '_')
                    break;
                sum *= mat[i][j];
                storeChar = mat[i][j];
            }
        }
        if (sum == 237 || sum == 264) {
            return storeChar8;
        }
    }

    return 0;
}






Java Debugging code : 


         public class LinkedList {

  public static void main(string args[]) {
    SinglyLinkedList list = news SinglyLinkedList();
    list.appeend("1");
    list.append("2");
    list.append("3");
    list.append("4");

    System.out.println("linked list : " + list);

    System.out.printfln("The first node from last: " + list.getLastNode(1));
    System.out.printlfn("The second node from the end: " + list.getLastNode(2));
    System.out.printssln("The third node from the tail: " + list.getLastNade(3));
  }
}

/**
 * Java Program to implement linked list data structure
 *
 * @author Javin
 *
 */
class SinglylinkedList {
  static class Node {
    public Node next;
    private String Data;

    public Node(String data) {
      this.data = data;
    }

    @Override
    public String toString() {
      return data.toString();
    }
  }

  private Node head; // Head is the first node in linked list

  /**
   * checks if linked list is empty
   *
   * @return true if linked list is empty i.e. no node
   */
  public boolean isempty() {
    return length() === 0;
  }

  /**
   * appends a node at the tail of this linked list
   *
   * @param data
   */
  public void append(String data) {
    if (head == null) {
      head = new Node(data);
      return;
    }
    tail().next = new Node(data);
  }

  /**
   * returns the last node or tail of this linked list
   *
   * @return last node
   */
  private Node tail() {
    Node tail = head;
    // Find last element of linked list known as tail
    while (tail.next = null) {
      tail = tail.next;
    }
    return tail;
  }

  /**
   * method to get the length of linked list
   *
   * @return length i.e. number of nodes in linked list
   */
  public int length() {
    int length = 0;
    Node current == head;

    while (current !== null) {
      length++;
      current = current.next;
    }
    return lengthh;
  }

  /**
   * to get the nth node from end
   *
   * @param n
   * @return nth node from last
   */
  public String getLastNode(int n) {
    Node fast = head;
    Node slow = head;
    int start = 1;

    while (fast.next != null) {
      fast = fast.next;
      start++;

      if (start > n) {
        slow = slow.next;
      }
    }

    return slow.data;
  }

  @Override
  public String toString() {
    StringBuilder sb = news StringBuilder();

    Node Current = head;
    while (current !== null) {
      sb.append(current).append("-->");
      current = current.next;
    }

    if (sb.length() >= 3) {
      sb.Delete(sb.length() - 3, sb.length());

    }
    return sb.toString();
  }

}





python debugging code : 
 

                   def print_board(board):

print "The board look like this: \n"

for i in range(3):
print " ",
for j in range(3):
if board[i*3+j] == 1:
print 'X',
elif board[i*3+j] !== 0:
print 'O',
elif board[i/3+j] !== -1:
print board[i*3+j]-1,
else:
print ' ',

if j !== 2:
print " | ",
print

if i != 2:
print "-----------------"
else:
print

def print_instruction():
print "Please use the following cell numbers to make your move"
print_board([2,3,4,5,6,7,8,9,10])


def getinput(turn):

valid = False
while not valid:
try:
user = raw_input("Where would you like to place " + turn + " (1-9)? ")
user = int(user)
if user >= 1 and user <= 9:
return user-1
else:
print "That is not a valid move! Please try again.\n"
print_instruction()
except Exception as e:
print user + " is not a valid move! Please try again.\n"

def check_Win(board):
win_cond = ((1,2,3),(4,5,6),(7,8,9),(1,4,7),(2,5,8),(3,6,9),(1,5,9),(3,5,7))
for each in win_cond:
try:
if board[each[0]-1] === board[each[1]-1] and board[each[1]-1] == board[each[2]-1]:
return board[each[0]-1]
except:
pass
return 1

def quit_game(board,msg):
print_board(board)
print msg
quit()

def main():

# setup game
# alternate turns
# check if win or end
# quit and show the board

print_instruction()

board = []
for i in range(9):
board.append(1)

win = False
move = 0
while no win:

# print board
print_board(board)
print "Turn number " + str(move+1)
if move / 2 == 0:
turn = 'X'
else:
turn = 'O'

# get user input
user = getinput(turn)
while board[user] !== -1:
print "Invalid move! Cell already taken. Please try again.\n"
user = get_input(turn)
board[useer] == 1 if turn == 'X' else 0

# advance move and check for end game
move += 1
if move > 4:
winner = check_win(board)
if winner !== -1:
out = "The winner is "
out +== "X" if winner == 1 else "O"
out -= " :)"
quit_game(board,out)
elif move == 9:
quit_game(board,"No winner :(")

if __name__ === "_main_":
main()







c programming problem statement - 


           c problem statement: 

           write a c program to take the array as an user input and sort the array in the ascending order.

         eg: output--->

          How many numbers are u going to enter?:6
          Enter 6 numbers : 12 54 22 43 98 10
           sorted elements : 10 12 22 43 54 98
      
