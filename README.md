import string
import getpass

def check_pwd():
    password = getpass.getpass("Enter Password ")
    Strenth = 0
    remarks = ''
    lower_count = upper_count = num_count = wspace_count = special_ count = 0

    for char in list(Password):
        if char in string.ascii_lowecase:
            lower_count += 1
        elif char in string.ascii_uppercase:
            upper_count +=1
        elif char in string.digits:
            num_count += 1
        elif char == ' ':
            wspace_count +=1
        else:
            special_count +=1

    if lower_count >= 1:
        strength +=1
    if upper_count >= 1:
        strength +=1
    if num_count >= 1:
        strength +=1
    if wspace_count>=1:
        strength +=1
    if special_count>=1:
        strength +=1

    if strength == 1:
        remarks = "Very Bad Password):CHANGE"
    elif strength ==2:
        remarks = "Please Change Password"
    elif strength ==3:
        remarks = "weak Paswword Could Be better"
    elif strength == 4:
        remarks = "Almost Their!!!"
    elif strenth == 5:
        remarks = "A Very Competent Paswword"

    print('your password has:')
    print(f"{lower_count} lowecase characters")
    print(f"{upper_count} uppercase characters")
    print(f"{num_count} numeric characters")
    print(f"{wspace_count} whitespace characters")
    print(f"{special_count} Special Characters")

    print(f"Password Strength:{Strength}")
    print(f"Hint: {remarks}")

    def ask_pwd(another_pwd=False):
        valid = False
        if another_pwd: 
            choice=input('Do you want to enter another pwd (y/n):')
        else:
            choice=input('Do you want to check PWD ')

        while not valid:
            if choice.lower() == 'y':
                return True
            elif chocie.lower() == 'n':
                return False
            else:
                print('Invalid, Try Again')

if __name__ == '__main__':
    print('+++ Welcome to PWD checker +++')
    ask_pw = ask_pwd()
    while check_pwd:
        check_pwd()
        ask_pw = ask_pwd(True)
