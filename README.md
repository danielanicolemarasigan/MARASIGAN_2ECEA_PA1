# MARASIGAN_2ECEA_PA1

This repository contains python scripts/codes solving the 3 different given problems in my programming assignment on the Introduction to Python Programming.

---

## Files
* 'MARSIGAN_2ECEA_PA1.ipynb': This Jupyter Notebook file contains the codes for each problem.
* 'README.md': This file contains the summary of the assignment.

---

## Solutions Overview
### 1. Alphabet Soup Problem

**Problem:** Create a function that takes a string and returns a string with its letters in alphabetical order.

**Approach:**
1. The program prompts the user to type in a a word, which then will be stored as a string (p)
2. The string (p) will then be converted into a list of characters.
3. The list of characters will then be sorted alphabetically by the .sort function
4. It now then prints the result, the word's letters being arranged alphabetically.

<pre>p = input("Enter a word: ") #Prompts the user to type in a word, stored in variable p as a string
alphabet_soup = list(p) #String (p) will be converted into a list of characters (e.g. hello - will be listed letter per letter; h, e, l, l, o)
alphabet_soup.sort() #The list of characters will be sorted alphabetically, then stored in the variable alphabet_soup

print(alphabet_soup) #This prints the result, stored in the alphabet_soup variable, each character arranged alphabetically </pre>

---

## 2. Emoticon Problem
**Problem:** Create a function that takes and replaces particular words into emoticons.

**Approach:**
1. The code defines the function 'emotify' then accepts the string (sentence) as its input.
2. A dictionary is then made containing specific words with their corresponding emoticons.
3. The input sentence is then converted into a list of words using the .split function
4. The resulting list of words is then stored in an empty list.
5. Using the for loop containing if-else statements, this part of the code loops each word to check for matches in the words placed in the dictionary.
6. If a match is found, then that word will be replaced by its corresponding emoticon using the append function.
7. If the word does not match any of the words in the dictionary, then it is left as it is.
8. The sentence will now be in a new single string, with specific words included in the dictionary replaced as emoticons.

<pre>def emotify(sentence): #Code starts with an own-made function, accepting the string (sentence) as its input
  emoticons_dict = { "smile": ":)","Smile": ":)", "grin": ":D","Grin": ":D","sad": ":((", "Sad": ":((", "mad": ">:(", "Mad": ">:("} #Dictionary emotions_dict contains emotions (serving as keys) corresponding with their emoticons (as the pair values)
  
  words_list = sentence.split() #The string (sentence) is split into a list of words
  result_list = [] #The resulting list of words is then stored in this list
  
  for word in words_list:
    if word in emoticons_dict:
      result_list.append(emoticons_dict[word])
    else:
      result_list.append(word)
      
  return " ".join(result_list)
    
print(emotify("I am so Mad"))
print(emotify("Make me Grin"))
print(emotify("I love to smile"))
print(emotify("It's okay to be sad"))</pre>
---

## 3. Unpacking List Problem
**Problem:** Given a list, create a code that divides the list into three variables: the first, the middle, and the last element -- having your middle element being everything in between the first and last element.

**Approach:** 
1. A list is created, consisting of numbers 1-6.
2. In printing the first element, we consider that lists in Python are zero-indexed. With that, the first element is located at index 0. 2
3. Printing the middle elements would then involve incorporating indices 1 to 5, denoted as list[1:5] to print the 2nd element (located at index 1) to the 5th element (located at index 4).
4. In printing the last element, we then indicate it as the element located at index 5.

<pre>list = [1, 2, 3, 4, 5, 6]
print("first: " , list[0])
print("middle: ", list[1:5])
print("last: ", list[5])</pre>
---

## How to View:

The Notebook file may be previewed via Github, or may be imported as an .ipynb file to Jupyter Notebook in order to see the full code with its input & output.

