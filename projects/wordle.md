```python
def match(guess, answer):
    pattern = [ "3","3","3","3","3" ]
    matches = []
    stringPattern = ''
    
    # matches will contain all positions of the answer which match some
    # position in the guess. Every position in matches will only be associated
    # with one position of the guess.
    
    # wordleList included every valid word from New York Time's library
    #while guess not in wordleList:
    #    guess = input()
    
    # first pass
    for letter in range(len(answer)):
        if guess[letter] == answer[letter]:
            pattern[letter] = "2"
            matches.append(letter)
        elif guess[letter] not in answer:
            pattern[letter] = "0"
        else:
            # we mark anything not 0 or 2.
            pattern[letter] = "3"
    
    # at this point matches contains every position that has a 2
    # guess: sissy
    # answer: bless
    # Ex: ['3','0','3','2','0']
    
    # second pass
    for letter in range(len(answer)):
        if pattern[letter] == "3":
            dummy = 0
            # we only reach here if guess[letter] != answer[letter] 
            # and guess[letter] is somewhere else in the answer 
            for dummy in range(len(answer)):
                if dummy not in matches:
                    if guess[letter] == answer[dummy]:
                        pattern[letter] = "1"
                        matches.append(dummy)
    
    # matches now assigns 1 to every 3 that is in the answer, but not the
    # correct position.
    # guess: sissy
    # answer: bless
    # Ex: ['1','0','3','2','0']
        
    # third pass
    for letter in range(len(answer)):
        if pattern[letter] == "3":
            pattern[letter] = "0"
    
    # matches now assigns 0 to the remaining 3's
    # guess: sissy
    # answer: bless
    # Ex: ['1','0','0','2','0']
    
    # makes pattern a string
    for letterMatch in range(len(pattern)):
        stringPattern += pattern[letterMatch]
    
    return stringPattern

guess = 'guess'
answerWord = "bless"

match(guess, answerWord)
```




    '00222'



def match(guess, answer):
    pattern = [ "3","3","3","3","3" ]
    matches = []
    stringPattern = ''
    
    # matches will contain all positions of the answer which match some
    # position in the guess. Every position in matches will only be associated
    # with one position of the guess.
    
    # wordleList included every valid word from New York Time's library
    #while guess not in wordleList:
    #    guess = input()
    
    # first pass
    for letter in range(len(answer)):
        if guess[letter] == answer[letter]:
            pattern[letter] = "2"
            matches.append(letter)
        elif guess[letter] not in answer:
            pattern[letter] = "0"
        else:
            # we mark anything not 0 or 2.
            pattern[letter] = "3"
    
    # at this point matches contains every position that has a 2
    # guess: sissy
    # answer: bless
    # Ex: ['3','0','3','2','0']
    
    # second pass
    for letter in range(len(answer)):
        if pattern[letter] == "3":
            dummy = 0
            # we only reach here if guess[letter] != answer[letter] 
            # and guess[letter] is somewhere else in the answer 
            for dummy in range(len(answer)):
                if dummy not in matches:
                    if guess[letter] == answer[dummy]:
                        pattern[letter] = "1"
                        matches.append(dummy)
    
    # matches now assigns 1 to every 3 that is in the answer, but not the
    # correct position.
    # guess: sissy
    # answer: bless
    # Ex: ['1','0','3','2','0']
        
    # third pass
    for letter in range(len(answer)):
        if pattern[letter] == "3":
            pattern[letter] = "0"
    
    # matches now assigns 0 to the remaining 3's
    # guess: sissy
    # answer: bless
    # Ex: ['1','0','0','2','0']
    
    # makes pattern a string
    for letterMatch in range(len(pattern)):
        stringPattern += pattern[letterMatch]
    
    return stringPattern

guess = 'guess'
answerWord = "bless"

match(guess, answerWord)
