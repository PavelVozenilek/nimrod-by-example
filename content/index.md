---
title: Main
---

# Nimrod by Example

Nimrod is a powerful statically typed language that allows the programmer expressiveness without compromising run-time performance.

``` nimrod
import tables, strutils

var wordFrequencies = initTable[string, int]

for line in stdin.lines:
  for word in line.split(", "):
    wordFrequencies[word] += 1

var maxFrequency = 0
var mostFrequentWord: string
for word, frequency in wordFrequencies:
  if frequency > maxFrequency:
    maxFrequency = frequency
    mostFrequentWord = word

echo "The most frequent word is '", word, "'"
```