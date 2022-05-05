# Code
```py
class quiz49:
    '''Define the attribute of the class which will be in string'''
    def __init__(self,binary:str):
        self.binary = binary
    '''Method to change the binary code to unary code'''
    def Unary_encoder(self):
        '''Create variables for iterations and result'''
        result = ""
        i=0
        '''Use while loop to repeat which will act similar to for loop but has been chosen in this case because it doesn't reset the i when 
        the loop start again'''
        while i < (len(self.binary)):
            '''For the number in that index to be 1, one 0 with space will be added into the result variable'''
            if self.binary[i]== "1" :
                result += "0 "
                '''This while loop will count how many 1 in a row and add them after the first 0 which number of zeros will tell the number of 
                ones.'''
                while i < len(self.binary) and self.binary[i]  == "1":
                    result += "0"
                    '''Change the index until the next number is 0'''
                    i+=1
            elif self.binary[i]=="0":
                '''Same apply for 0 which will added two zeros and space into the result variable.'''
                result += "00 "
                while  i < len(self.binary) and self.binary[i]=="0":
                    result += "0"
                    i+=1

            result += " "
            '''After each loop a space will be added'''

        return result
        '''Then return the final result after the convertion'''

test1 = quiz49("1000011")
test2 = quiz49("1111011")
test3 = quiz49("111")
test4 = quiz49("100")
print(test1.Unary_encoder())
print(test2.Unary_encoder())
print(test3.Unary_encoder())
print(test4.Unary_encoder())




```

# Test

<img width="151" alt="Quiz49" src="https://user-images.githubusercontent.com/82266864/166855110-598551fd-d476-442b-a917-7b7b2ed87322.png">
