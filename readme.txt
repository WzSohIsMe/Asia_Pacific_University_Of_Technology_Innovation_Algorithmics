# Automated Tool For Algorithmics Visualization
This tool is designed for computer science students that are lazy to insert value one by one on University of San Francisco Visualization Tool.

# Available Links
- B-Tree Visualization - https://www.cs.usfca.edu/~galles/visualization/BTree.html
- B+Tree Visualilzation - https://www.cs.usfca.edu/~galles/visualization/BPlusTree.html
- Binomial Queue Visualization - https://www.cs.usfca.edu/~galles/visualization/BinomialQueue.html


# Follow these steps
1. Change the items of the keys=[1,2,3,4,5,6,7,8,9,10]
2. Copy the script
3. Visit the link above
4. Right-click and choose "Inspect Element"
5. Choose "Console" tab
6. Paste the script and press Enter
7. Enjoy


# Script
```javascript
// Define the keys array
var keys = [3, 6, 2, 8, 2, 9];

// Function to insert numbers one by one
function insertNumbers(index) {
  // Get the input field and insert button by their IDs or other selectors
  var inputField = document.querySelector('#AlgorithmSpecificControls input[type="text"]');
  var insertButton = document.querySelector('#AlgorithmSpecificControls input[type="button"]');

  // Check if there are still numbers to insert
  if (index < keys.length) {
    // Set the value of the input field
    inputField.value = keys[index];

    // Click the "Insert" button
    insertButton.click();

    // Increment the index for the next number
    index++;

    // Wait for the animation to complete (adjust the timeout as needed)
    setTimeout(function () {
      // Recursively call the function for the next number
      insertNumbers(index);
    }, 1500); // Adjust the timeout as needed
  }
}

// Start inserting numbers from the beginning of the keys array
insertNumbers(0);
