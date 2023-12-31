Describe: wordCounter()

Test #1: "It should return 1 if a passage has just one word."
Code:
const text = "hello";
wordCounter(text);
Expected Output: 1

Test #2: "It should return 2 if a passage has two words."
Code:
const text = "hello there";
wordCounter(text);
Expected Output: 2

Test #3: "It should return 0 for an empty string."
Code: wordCounter("");
Expected Output: 0

Test #4: "It should return 0 for a string that is only spaces."
Code: wordCounter("            ");
Expected Output: 0

Test #5: "It should not count numbers as words."
Code: wordCounter("hi there 77 19");
Expected Output: 2


Describe: numberOfOccurencesInText()

Test #1: "It should return 0 occurences of a word for an empty string."
Code:
const text = "";
const word = "red";
numberOfOccurrencesInText(word, text);
Expected Output: 0

Test #2: "It should return 1 occurrence of a word when the word and the text are the same."
Code:
const text = "red";
const word = "red";
numberOfOccurrencesInText(word, text);
Expected Output: 1

Test #3: "It should return 0 occurrences of a word when the word and the text are different."
Code:
const text = "red";
const word = "blue";
numberOfOccurrencesInText(word, text);
Expected Output: 0

Test #4: "It should return the number of occurrences of a word."
Code:
const text = "red blue red red red green";
const word = "red";
numberOfOccurrencesInText(word, text);
Expected Output: 4

Test #5: "It should return a word match regardless of case."
Code:
const text = "red RED Red green Green GREEN";
const word = "Red";
numberOfOccurrencesInText(word, text);
Expected Output: 3

Test #6 : "It should return a word match regardless of punctuation."
Code:
const text= "Red! Red. I like red, green, and yellow.";
const word="Red";
numberOfOccurancesInText(word, text);
Expected Output: 3;

Test #7: "It should not return a word match if word is included within a different part of different word within the same text."
Code:
const text = "I had to redo the red project, redos suck!";
const word = "Red";
numberOfOccurancesInText(word, text);
Expected Output: 1;

Describe: swearWords()

Test #1: "It should omit the words "loopdaloop", "zoinks", "muppeteer","biffaroni" from a word input"
const text = "zoinks scooby!"
swearWords(text);
Expected output: 1

Describe: boldPassage()

Test #1: "It should return null if no word or text is entered."
Code:
const text = "";
const word = "";
boldPassage(word, text);
Expected Output: null


Test #2: "It should return a non-matching word in a p tag."
Code:
const word = "hello";
const text = "yo";
boldPassage(word, text);
Expected Output: <p>yo</p>

Test #3: "It should return a matching word in a strong tag."
Code:
const word = "hello";
const text = "hello";
boldPassage(word, text);
Expected Output: <p><strong>hello</strong></p>

Test #4: "It should wrap words that match in strong tags but not words that don't."
Code:
const word = "hello";
const text = "hello there";
boldPassage(word, text);
Expected Output: <p><strong>hello</strong> there</p>
