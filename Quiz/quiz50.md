```py
class quiz50:
    def __init__(self,  message:str):
        # attribute of the class which is the message and the list of each alphabet in ascii
        self.alphabet = [
            "### ##   ## ##  ### ###  ## # # ###  ## # # #   # # ###  #  ##   #  ##   ## ### # # # # # # # # # # ### ###",
            "# # # # #   # # #   #   #   # #  #    # # # #   ### # # # # # # # # # # #    #  # # # # # # # # # #   #   # ",
            "### ##  #   # # ##  ##  # # ###  #    # ##  #   ### # # # # ##  # # ##   #   #  # # # # ###  #   #   #   ## ",
            "# # # # #   # # #   #   # # # #  #  # # # # #   # # # # # # #    ## # #   #  #  # # # # ### # #  #  #       ",
            "# # ##   ## ##  ### #    ## # # ###  #  # # ### # # # #  #  #     # # # ##   #  ###  #  # # # #  #  ###  #  "
        ]
        self.message = message

        #method that will convert the inputted alphabet to ascii art
    def ascii_art(self):
        #create list with 5 items to input each line of the ascii
        result = ["" for a in range(5)]
        # loop for the length of the message
        for i in range (len(self.message)):
            #convert the alphabet to ascii decimal
            n = ord(self.message[i])
            #convert letter to number between 1-26
            if n<=90 and n>=65:
                n -=64

            elif n<=122 and n>=97:
                n-=96
            #when the it's not letter the number will be 27
            else:
                n = 27
            # for every line it will take what is in the each line 
            for k in range(5):
                letter = self.alphabet[k]
                result[k]+=letter[(n-1)*4:n*4]
        # join each item together and make new line for every item
        final = ("\n".join(result))
        #return final result
        return final

test1 = quiz50(message="E")
test2 = quiz50(message="gOLDen")
test3 = quiz50(message="ManhAtTan")
test4 = quiz50(message="ManhAtTa=")
print(test1.ascii_art())
print(test2.ascii_art())
print(test3.ascii_art())
print(test4.ascii_art())

```



# Test
