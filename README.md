Problem Description  
Julius Caesar lives in an age of danger and conspiracy. In order to survive, he first invented the password for military messaging. Suppose you are an officer in the Caesar Legion. You need to decipher the message sent by Caesar and provide it to your general. The method of message encryption is to replace each letter in the original text of the message with the fifth letter after the letter (for example, each letter A in the original text of the message is replaced by the letter F), and the other characters are unchanged. And all the letters of the original text of the message are capitalized. The correspondence between the letters in the password and the letters in the original text is as follows.
  
Password letters: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z  
Original letter: V W X Y Z A B C D E F G H I J K L M N O P Q R S T U  
Input: Up to 100 data sets. Each data set consists of 3 parts  
Start line: START  
Password message: A line of 1 to 200 characters representing a message from Caesar  
End line: END  
After the last data set, there is another line: ENDOFINPUT  
Output: One row for each data set, which is Caesar's original message.  
  
Input sample  
START  
NS BFW, JAJSYX TK NRUTWYFSHJ FWJ YMJ WJXZQY TK YWNANFQ HFZXJX  
END  
START  
N BTZQI WFYMJW GJ KNWXY NS F QNYYQJ NGJWNFS ANQQFLJ YMFS XJHTSI NS  
WTRJ  
END  
START   
IFSLJW PSTBX KZQQ BJQQ YMFY HFJXFW NX RTWJ IFSLJWTZX YMFS MJ  
END  
ENDOFINPUT  
  
Output sample  
IN WAR, EVENTS OF IMPORTANCE ARE THE RESULT OF TRIVIAL CAUSES  
I WOULD RATHER BE FIRST IN A LITTLE IBERIAN VILLAGE THAN SECOND IN ROME  
DANGER KNOWS FULL WELL THAT CAESAR IS MORE DANGEROUS THAN HE  
  
problem analysis  
This problem is very simple, and each letter in the password message can be transformed accordingly. The key is to identify the message lines in the input data and the data in the message lines. In the input data, each message line includes multiple words, and several punctuation marks.  
(1) When the scanf function enters a string, there can be no spaces in each string. Every time the word "START" is read, it means that the words in a message line are read until the word "END" is read.  
(2) When decrypting a message, you need to change the string of the word in the message as a normal array, and then transform each letter in turn.  
  
solution  
After reading the message line, read each word in it by scanf and decrypt it separately. The decrypted words are spliced into a complete message in the original order. The following string handlers are required:  
Strcmp: recognizes the start and end of the message line in the input data  
Strlen: Calculate the length of each word in the encrypted message  
Strcat: re-splicing the decrypted words into a complete message  
  
Common mistakes  
(1) When reading a word in a password message, the punctuation after the word is also read into the string cipher along with the word. For example, the first message in the input sample, the second word is followed by the punctuation ",", and when the word "BFW" is read, the string actually read in the cipher is "BFW,". When decrypting a message, the non-letter symbol in the cipher is identified, and only the alphabetic symbols are transformed.  
(2) When a word is read from a password message, the space symbol between words is ignored. When generating a restored message, insert a space symbol between different words.  
  
