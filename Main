/* Matthew Young
 
 * This program will evaluate a user inputed RPN expression using stacks.
 
 */


#include<iostream>
#include<stack>
#include<string>

using namespace std;

int EvaluateRpnExpression(string rpnExpression); // Lines 41-44: Functions to evaluate the expression
int getAnswer(char mathOperator, int operation1, int operation2);
bool mathOperation(char Y);
bool Number(char Y);

int EvaluateRpnExpression(string rpnExpression)
{
    stack<int> myStack;
    
    for(int i = 0; i < rpnExpression.length(); i++) { // Loop to evaluate expression
        
        if(rpnExpression[i] == ' ');
        
        else if(mathOperation(rpnExpression[i])) {
            
            int operation2 = myStack.top(); // Set top of stack = to int
            myStack.pop();                  // Remove top of stack
            
            int operation1 = myStack.top(); // Set top of stack = to int
            myStack.pop();                  // Remove top of stack
            
            int answer = getAnswer(rpnExpression[i], operation1, operation2);
            
            myStack.push(answer); // Insert evaluated expression into stack
            new stack<int>; 
        }
        
        else if(Number(rpnExpression[i])){
            
            int operators = 0;
            
            while(i<rpnExpression.length() && Number(rpnExpression[i])) {
                
                operators = (operators * 10) + (rpnExpression[i] - '0');
                i++;
            }
            
            i--;
            cout << "Token = " << operators << " Push " << operators << endl;
            myStack.push(operators);
        }
    }
    
    return myStack.top();
}


bool Number(char Y){ // Check if value is a number
    
    if(Y >= '0' && Y <= '9'){
        
        return true;
    }
    
    return false;
}


bool mathOperation(char Y){ // Check if value is a math operation
    
    if(Y == '+' || Y == '-' || Y == '*' || Y == '/'){
        return true;
    }
    
    return false;
}


int getAnswer(char mathOperator, int operation1, int operation2){ // Lines 111-134 perform operations
    
    if(mathOperator == '+'){
        cout << "Token = + Pop " << operation2 << " Pop " << operation1;
        cout << " Push " << (operation1 + operation2) << endl;
        
        return operation1 + operation2;
    }
    
    else if(mathOperator == '-'){
        cout << "Token = - Pop " << operation2 << " Pop " << operation1;
        cout << " Push " << (operation1 - operation2) << endl;
        
        return operation1 - operation2;
    }
    
    else if(mathOperator == '*'){
        cout << "Token = * Pop " << operation2 << " Pop " << operation1;
        cout << " Push " << (operation1 * operation2) << endl;
        
        return operation1 * operation2;
    }
    
    else if(mathOperator == '/'){
        cout << "Token = / Pop " << operation2 << " Pop " << operation1;
        cout << " Push " << (operation1 / operation2) << endl;
        
        return operation1 / operation2;
    }
    
    else cout << "Error invalid input! " << endl;
    
    return 0;
}

int main(){



    string rpnExpression;
    char progContinue;
    
    cout<<"Please enter the RPN expression to be evaluated: ";
        getline(cin, rpnExpression);
    
    int answer = EvaluateRpnExpression(rpnExpression);
    
    cout<< "Token = Pop " << answer << endl;
    
    cout << "Type 'Y' or 'y' to continue or type any other letter to quit: ";
    cin >> progContinue;

    while(progContinue == 'Y' || progContinue == 'y') {
        string rpnExpression2;
        
        cout << "Please enter the RPN expression to be evaluated: ";
            getline(cin, rpnExpression2);
        
        int answer = EvaluateRpnExpression(rpnExpression2);
        
        cout << "Token = Pop " << answer << endl;
        
        cout << "Type 'Y' or 'y' to continue or type any other letter to quit: ";
        cin >> progContinue;
    }
    
    if (progContinue != 'Y' || progContinue != 'y') {
        return 0;
    }
    
    return 0;
}
