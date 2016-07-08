# Code-To-Work: Ghost 

This workshop's activity is a game called Ghost.

Ghost is a word game in which players take turns adding individual letters to a growing word fragment, trying not to be the one to complete a valid word. Each fragment must be the beginning of an actual word, and, for our purposes, we will consider 4 to be the minimum word length. The player who completes a word or creates a fragment that is not the prefix of a word loses the round.

So on player 1's turn, they can:
 + challenge player 2's word if they think player 2 has formed a valid word of at least 4 letters. 
 + If the fragment is a word, then player 1 wins; if the fragment is not a word, then player 2 wins. 
 + challenge player 2's word if they think that no word can be formed with the current fragment. Then, player 2 must provide a valid word starting with the current fragment or lose.
 + add a letter to move the fragment towards a valid word 
 + attempt to bluff player 2 by adding a letter that doesn't move the fragment towards a valid word

## User Interface
![UI](https://github.com/Hitscotty/Ghost/blob/master/ghost.png)

## Tour of Code 

+ GhostDictionary: Note that this is an interface, not a class. This is the shared interface for SimpleDictionary and FastDictionary. This shared interface makes it easy to swap between the two kinds of dictionaries in the activity.
+ SimpleDictionary: This is an implementation of the dictionary that stores the words in an ArrayList.
+ getAnyWordStartingWith: will naively use binary search to look for some word that starts with the given prefix.
+ getGoodWordStartingWith: will still use binary search but will try to make a smarter word selection than getAnyWordStartingWith
+ FastDictionary: This is an implementation of our dictionary that stores the words in a trie (we will implement this in the next unit). The interface is the same as SimpleDictionary and the given implementation is complete as all the actual functionality goes into the TrieNode class.
+ TrieNode: Used to create a graph of strings, each char being a node and the leafs being words. Each node has a boolean that dictates whether the path up to that char is a word. 



[Further Description of Project here][android]



[android]: https://cswithandroid.withgoogle.com/content/unit?unit=7&lesson=9
