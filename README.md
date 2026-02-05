#include <iostream>
#include <vector>
#include <string>
#include <algorithm>

using namespace std;

// 1. Sum of two integers
int sum(int x, int y) {
    return x + y;
}

// 2. Count vowels in a string
int countVowels(string text) {
    int count = 0;
    for (char c : text) {
        if (c=='a'||c=='e'||c=='i'||c=='o'||c=='u'||
            c=='A'||c=='E'||c=='I'||c=='O'||c=='U') {
            count++;
        }
    }
    return count;
}

// 3. Average of integers in a list
double average(vector<int> numbers) {
    int total = 0;
    for (int n : numbers) {
        total += n;
    }
    return (double)total / numbers.size();
}

// 4. Remove vowels from a sentence
string removeVowels(string sentence) {
    string result = "";
    for (char c : sentence) {
        if (!(c=='a'||c=='e'||c=='i'||c=='o'||c=='u'||
              c=='A'||c=='E'||c=='I'||c=='O'||c=='U')) {
            result += c;
        }
    }
    return result;
}

// 5. Longest string in a list
string longestString(vector<string> words) {
    string longest = words[0];
    for (string w : words) {
        if (w.length() > longest.length()) {
            longest = w;
        }
    }
    return longest;
}

// 6. Median of a list of integers
double median(vector<int> numbers) {
    sort(numbers.begin(), numbers.end());
    int n = numbers.size();

    if (n % 2 == 0)
        return (numbers[n/2 - 1] + numbers[n/2]) / 2.0;
    else
        return numbers[n/2];
}

// 7. Remove even numbers from a list
vector<int> removeEven(vector<int> numbers) {
    vector<int> result;
    for (int n : numbers) {
        if (n % 2 != 0) {
            result.push_back(n);
        }
    }
    return result;
}

// 8. Sort strings alphabetically
vector<string> sortStrings(vector<string> words) {
    sort(words.begin(), words.end());
    return words;
}

// 9. Sum of integers in a list
int sumList(vector<int> numbers) {
    int total = 0;
    for (int n : numbers) {
        total += n;
    }
    return total;
}

// 10. Reverse all strings in a list
vector<string> reverseStrings(vector<string> words) {
    for (string &w : words) {
        reverse(w.begin(), w.end());
    }
    return words;
}

int main() {
    // Program runs without errors
    cout << "Assignment 3 Functions Compiled Successfully." << endl;
    return 0;
}
