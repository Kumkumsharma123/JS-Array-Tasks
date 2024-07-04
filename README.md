# JS-Array-Tasks
# 1. Join elements of an array into a string
let myColor = ["Red", "Green", "White", "Black"];
console.log(myColor.join(","));
console.log(myColor.join(","));
console.log(myColor.join("+"));

# 2. Find the most frequent item of an array
let arr1 = [3, 'a', 'a', 'a', 2, 3, 'a', 3, 'a', 2, 4, 9, 3];

function mostFrequent(arr) {
    let frequency = {};
    let maxCount = 0;
    let mostFrequentItem;

    for (let i = 0; i < arr.length; i++) {
        let item = arr[i];
        if (frequency[item] == null) {
            frequency[item] = 1;
        } else {
            frequency[item]++;
        }

        if (frequency[item] > maxCount) {
            maxCount = frequency[item];
            mostFrequentItem = item;
        }
    }
    
    return mostFrequentItem + " ( " + maxCount + " times )";
}

console.log(mostFrequent(arr1));

# 3. Truncate a string
function truncateString(str, num) {
    return str.length > num ? str.slice(0, num) : str;
}

console.log(truncateString("Robin Singh", 4));

// 4. Capitalize words in a string
function capitalizeWords(str) {
    return str.split(' ').map(word => word.charAt(0).toUpperCase() + word.slice(1)).join(' ');
}

console.log(capitalizeWords('js string exercises'));

# 5. Find elements between two numbers in an array
function arrBetween(a, b, arr) {
    return arr.filter(item => item > a && item < b);
}

console.log(arrBetween(3, 8, [1, 5, 95, 0, 4, 7])); // ➞ [5, 4, 7]
console.log(arrBetween(1, 10, [1, 10, 25, 8, 11, 6])); // ➞ [8, 6]
console.log(arrBetween(7, 32, [1, 2, 3, 78])); // ➞ []

# 6. Find the index of a value in an array
function findIndex(arr, value) {
    return arr.indexOf(value);
}

console.log(findIndex(["hi", "edabit", "fgh", "abc"], "fgh")); // ➞ 2
console.log(findIndex(["Red", "blue", "Blue", "Green"], "blue")); // ➞ 1
console.log(findIndex(["a", "g", "y", "d"], "d")); // ➞ 3
console.log(findIndex(["Pineapple", "Orange", "Grape", "Apple"], "Pineapple")); // ➞ 0
