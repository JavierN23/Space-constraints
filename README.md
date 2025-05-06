# Space-constraints

Following is the 'Word Builder' algorithm. Describe its space complexity in terms of Big O.

    function wordBuilder(array) { 
		let collection = [];
		for(let i = 0; i < array.length; i++) { 
				for(let j = 0; j < array.length; j++) {
						if (i !== j) {
								collection.push(array[i] + array[j]);
						}
				}
		}
		return collection; 
    }
Outer loop runs n amount of time. Inner loop runs n amount of times. The number of combination will be n * (n - 1). meaning the time complexity will be O(n^2). The reason it's not O(n) is because the number of items stores isn't proportional to the input size it's to the square input size. 


Following is a function that reverses an array. Describe its space complexity in terms of Big O:

    function reverse(array) { 
		let newArray = [];
		for (let i = array.length - 1; i >= 0; i--) { 
				newArray.push(array[i]);
		}
		return newArray;
    }    

Once it has an input, this code loops through an empty array and adds it to the new array. Then, it prints it in reverse. As n increases, the size of the new array increases linearly, therefore having a time complexity of O(n).

Create a new function to reverse an array that takes up just O(1) extra space.

	function doubleArray1(array) {
	let newArray = [];
	for (let i = 0; i < array.length; i++) {
		newArray.push(array[i] * 2);
	}
	return newArray;
	}




Following are three different implementations of a function that accepts an array of numbers and returns an array containing those numbers multiplied by 2. For example, if the input is [5, 4, 3, 2, 1], the output will be [10, 8, 6, 4, 2].
function doubleArray1(array) { 
	let newArray = [];

	for(let i = 0; i < array.length; i++) { 
		newArray.push(array[i] * 2);
	}
	return newArray; 
    }
    function doubleArray2(array) {
	for(let i = 0; i < array.length; i++) {
  	array[i] *= 2;

    }
	return array; 
    }
    function doubleArray3(array, index=0) { 
	if (index >= array.length) { return; }
    array[index] *= 2;
    doubleArray3(array, index + 1);
	return array; 
    }

![Space constraints drawio](https://github.com/user-attachments/assets/1b3f855f-8a57-4dcb-9f01-8d151f6dd54f)
