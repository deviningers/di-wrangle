# di-wrangle

## Play
*The Merry Wives of Windsor*

## Speakers
- speaker 1: SLENDER
- speaker 2: BARDOLPH 

## Question
**Who spoke more times, SLENDER or BARDOLPH?**

## Commands
Copy the full text of **The Merry Wives of Windsor**:
```bash
curl http://shakespeare.mit.edu/merry_wives/full.html | sed 's/<\/*[^>]*>//g' > merryWives.txt
cat merryWives.txt #to ensure it was copied correctly 
```
Count the number of times each person spoke:
```bash
cat merryWives.txt | grep "^SLENDER$" | wc -l > slenderCount.txt
cat merryWives.txt | grep "^BARDOLPH$" | wc -l > bardolphCount.txt
```
Compare the output of each 
```bash
echo "Slender talked:" >> results.txt
cat slenderCount.txt >> results.txt
echo "Bardolph talked:" >> results.txt
cat bardolphCount.txt >> results.txt
```

## Answer
Slender talked more. See results.txt for more info.
