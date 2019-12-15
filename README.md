# Substring Function
#1-prototype:
substring proto start:byte ,last:byte,input:ptr byte,output:ptr byte

# 2-Prerequisite:
to get a substring from a string pass it 4 arguments:
1st:symbol after which substring is required(excluding symbol itself)
2nd:symbol upto which substring is required(excluding symbol itself)
3rd:address of input string
4th:address of output string

# 3-Using method:
if first argument is zero '0' then it makes substring from starting
upto the second argument symbol

# 4-Instructions:
make variable symbol you want to use such as,but dont ake them null terminated
comma byte ','
dollar byte '$'

# Example code

.data

input byte 'sunslik shampoo,100$',0
output byte 30 dup(?),0
comma byte ','
dollar '$'
.code

invoke substring,0,comma,addr input,addr output    
;output will be substring -->sunslik shampoo

invoke substring ,comma,dollar,addr input,addr output 
;output will be substring --> 100


