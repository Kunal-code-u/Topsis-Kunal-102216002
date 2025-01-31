
# Topsis-Kunal-102216002

A Python package for **TOPSIS (Technique for Order of Preference by Similarity to Ideal Solution)** analysis.  
This tool evaluates and ranks alternatives based on multiple criteria, considering their relative closeness to an ideal solution.

## Installation

Use the package manager pip to install Topsis-Kunal-102216002.

```bash
  pip install Topsis-Kunal-102216002
```
    
## Usage
Enter csv filename followed by .csv extentsion, then enter the weights vector with vector values separated by commas, then enter the impacts vector with comma separated signs (+,-) followed by the name of output.csv file where you want to store the the output file.
```javascript
topsis sample.csv "1,1,1,1" "+,-,+,+" output.csv
```
To view usage help, use
```javascript
topsis /h
```

## Example
#### sample.csv

A csv file showing data for different mobile handsets having varying features.

| Attribute | Price | Storage | Camera | Looks |
|-----------|-------|---------|--------|-------|
| M1        | 250   | 16      | 12     | 5     |
| M2        | 200   | 16      | 8      | 3     |
| M3        | 300   | 32      | 16     | 4     |
| M4        | 275   | 32      | 8      | 4     |
| M5        | 225   | 16      | 16     | 2     |

weights vector = [ 0.25,0.25,0.25,0.25 ]

impacts vector = [ -,+,+,+]

## Input

```bash
topsis sample.csv "0.25,0.25,0.25,0.25" "+,+,-,+" output.csv
```

## Output

| Attribute | Price | Storage | Camera | Looks | Topsis Score   | Rank |
|-----------|-------|---------|--------|-------|----------------|------|
| M1        | 250   | 16      | 12     | 5     | 0.534276857    | 3    |
| M2        | 200   | 16      | 8      | 3     | 0.308367769    | 5    |
| M3        | 300   | 32      | 16     | 4     | 0.691632231    | 1    |
| M4        | 275   | 32      | 8      | 4     | 0.534736584    | 2    |
| M5        | 225   | 16      | 16     | 2     | 0.401046122    | 4    |


## Other notes
- The first column and first row are removed by the library before processing to eliminate indices and headers. Ensure that the CSV follows the format shown in `sample.csv`.
- Ensure the CSV does not contain categorical values.


## License

[MIT](https://www.mit.edu)
