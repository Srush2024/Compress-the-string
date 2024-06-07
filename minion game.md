#minion game

def minion_game(string):
    # your code goes here
    
    
    # Initialize the both scores at zero
    kev_scr = 0
    stu_scr = 0

### find the potential score of each letter in the word 
     # and add it to the correct score
    for letter_index in range(len(string)):
        pot_scr = len(string) - letter_index
        if string[letter_index] in 'AEIOU':
            kev_scr += pot_scr # kevin gets all words starting with a vowel
        else:
            stu_scr += pot_scr  # Stuart gets everything else 
    
    # Determine the winner, display their name and final score
    if kev_scr > stu_scr:
        print ("Kevin ", kev_scr, sep = "")
    elif kev_scr < stu_scr:
        print ("Stuart ", stu_scr, sep = "")
    else:
        print ("Draw")



if __name__ == '__main__':
    s = input()
    minion_game(s)
