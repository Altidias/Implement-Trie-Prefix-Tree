# Implement-Trie-Prefix-Tree
https://leetcode.com/problems/implement-trie-prefix-tree
# Intuition
<!-- Describe your first thoughts on how to solve this problem. -->
The Trie (prefix tree) data structure is well-suited for solving problems related to string prefixes. We can create a TrieNode that stores an array of children TrieNodes for each letter and a boolean value indicating whether the node is the end of a word. By implementing the Trie data structure, we can efficiently insert words, search for words, and check if a string starts with a given prefix.
# Approach
<!-- Describe your approach to solving the problem. -->
1. Create a TrieNode structure with an array of 26 children (one for each lowercase letter) and a boolean value is_end_of_word to indicate if the node is the end of a word.

2.  Initialize the Trie structure with a root TrieNode.

3. Implement the insert method to insert words into the Trie by iterating through the characters of the word and updating the children nodes accordingly. Set the is_end_of_word flag for the last character of the word.

4. Implement the search method to search for words in the Trie by iterating through the characters of the word and following the Trie structure. If a character is not found or the last TrieNode does not have the is_end_of_word flag set, return false; otherwise, return true.

5. Implement the starts_with method to check if a given prefix exists in the Trie by iterating through the characters of the prefix and following the Trie structure. If a character is not found, return false; otherwise, return true after the iteration.
# Complexity
- Time complexity:
<!-- Add your time complexity here, e.g. $$O(n)$$ -->
Insertion: $$O(L)$$, where $$L$$ is the length of the word being inserted.

Search: $$O(L)$$, where $$L$$ is the length of the word being searched.

Starts with: $$O(L)$$, where $$L$$ is the length of the prefix being checked.
- Space complexity:
<!-- Add your space complexity here, e.g. $$O(n)$$ -->
$$O(N * L)$$, where $$N$$ is the number of words and $$L$$ is the maximum length of a word. In the worst case, each word might not share any common prefix, requiring separate TrieNodes for each character.
