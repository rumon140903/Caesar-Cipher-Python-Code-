# Caesar-Cipher-Python-Code-
This is the python code of Caeser Cipher for encryption and decryption.


choice = input("Enter 1 to encryption or 2 to decryption: ")

alphabets= ["a", "b", "c", "d", "e", "f", "g", "h", "i", "j", "k", "l",
            "m", "n", "o", "p", "q", "r", "s", "t", "u", "v", "w", "x", "y", "z"]

if choice == "1":
    user = input("Enter the text you want to encrypt: ").lower()
    result=""
    key = int(input("Enter the key: "))
    for char in user:
        if char in alphabets:
           a = alphabets.index(char)
           add = (a + key) % 26
        alpha=alphabets[add]
        result += alpha
        
  
            
        print("The encrypted text is: ", result)
        
elif choice == "2":
    user = input("Enter the text you want to decrypt: ").lower()
    result=""
    key = int(input("Enter the key: "))

    
    for char in user:
        if char in alphabets:
            a = alphabets.index(char)
            sub = (a - key) % 26
            alpha=alphabets[sub]
            result += alpha
            
        else:
            result += char
    print("The decrypted text is: ", result)
    
else:
    print("Invalid choice. Please enter 1 for encryption or 2 for decryption.")
