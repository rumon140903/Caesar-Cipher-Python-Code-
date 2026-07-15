choice = input("Press 1 for encryption nor 2 for decryption: ")

alphabets= ["a", "b", "c", "d", "e", "f", "g", "h", "i", "j", "k", "l",
            "m", "n", "o", "p", "q", "r", "s", "t", "u", "v", "w", "x", "y", "z"]

if choice == "1":
    user = input("Plain text=P: ").lower()
    result=""
    key = int(input("Key=K: "))
    for char in user:
        if char in alphabets:
           a = alphabets.index(char)
           add = (a + key) % 26
        alpha=alphabets[add]
        result += alpha
        
  
            
        print("The encrypted text is: ", result)
        
elif choice == "2":
    user = input("Decryption text=D: ").lower()
    result=""
    key = int(input("Key=K: "))

    
    for char in user:
        if char in alphabets:
            a = alphabets.index(char)
            sub = (a - key) % 26
            alpha=alphabets[sub]
            result += alpha
            
        else:
            result += char
    print("Decrypted text=D: ", result)
    
else:
    print("Invalid choice. Please enter 1 for encryption or 2 for decryption.")

                
