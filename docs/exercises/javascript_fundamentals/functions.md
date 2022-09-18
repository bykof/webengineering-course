### 💻 Exercises

##### Exercises: Level 1

1. Declare a function _fullName_ and it takes firstName, lastName as a parameter and it returns your full - name.
2. Declare a function _addNumbers_ and it takes two two parameters and it returns sum.
3. Area of a circle is calculated as follows: _area = π x r x r_. Write a function which calculates \_areaOfCircle
4. Temperature in oC can be converted to oF using this formula: _oF = (oC x 9/5) + 32_. Write a function which convert oC to oF _convertCelciusToFahrenheit_.
5. Body mass index(BMI) is calculated as follows: _bmi = weight in Kg / (height x height) in m2_. Write a function which calculates _bmi_. BMI is used to broadly define different weight groups in adults 20 years old or older.Check if a person is _underweight, normal, overweight_ or _obese_ based the information given below.

   - The same groups apply to both men and women.
   - _Underweight_: BMI is less than 18.5
   - _Normal weight_: BMI is 18.5 to 24.9
   - _Overweight_: BMI is 25 to 29.9
   - _Obese_: BMI is 30 or more

6. Write a function called _checkSeason_, it takes a month parameter and returns the season:Autumn, Winter, Spring or Summer.

##### Exercises: Level 2

1. Quadratic equation is calculated as follows: _ax2 + bx + c = 0_. Write a function which calculates value or values of a quadratic equation, _solveQuadEquation_.

   ```js
   console.log(solveQuadratic()); // {0}
   console.log(solveQuadratic(1, 4, 4)); // {-2}
   console.log(solveQuadratic(1, -1, -2)); // {2, -1}
   console.log(solveQuadratic(1, 7, 12)); // {-3, -4}
   console.log(solveQuadratic(1, 0, -4)); //{2, -2}
   console.log(solveQuadratic(1, -1, 0)); //{1, 0}
   ```

2. Declare a function name _printArray_. It takes array as a parameter and it prints out each value of the array.
3. Write a function name _showDateTime_ which shows time in this format: 08/01/2020 04:08 using the Date object.

   ```sh
   showDateTime()
   08/01/2020 04:08
   ```

4. Declare a function name _swapValues_. This function swaps value of x to y.

   ```js
   swapValues(3, 4); // x => 4, y=>3
   swapValues(4, 5); // x = 5, y = 4
   ```

5. Declare a function name _reverseArray_. It takes array as a parameter and it returns the reverse of the array (don't use method).

   ```js
   console.log(reverseArray([1, 2, 3, 4, 5]));
   //[5, 4, 3, 2, 1]
   console.log(reverseArray(["A", "B", "C"]));
   //['C', 'B', 'A']
   ```

6. Declare a function name _capitalizeArray_. It takes array as a parameter and it returns the - capitalizedarray.
7. Declare a function name _addItem_. It takes an item parameter and it returns an array after adding the item
8. Declare a function name _removeItem_. It takes an index parameter and it returns an array after removing an ite
9. Declare a function name evensAndOdds . It takes a positive integer as parameter and it counts number of evens and odds in the number.

```sh
evensAndOdds(100);
The number of odds are 50.
The number of evens are 51.
```

13. Write a function which takes any number of arguments and return the sum of the arguments

```js
sum(1, 2, 3); // -> 6
sum(1, 2, 3, 4); // -> 10
```

1.  Declare a function name _userIdGenerator_. When this function is called it generates seven character id. The function return the id.

```sh
console.log(userIdGenerator());
41XTDbE
```

##### Exercises: Level 3

1. Declare a function name _userIdGeneratedByUser_. It doesn’t take any parameter but it takes two inputs using prompt(). One of the input is the number of characters and the second input is the number of ids which are supposed to be generated.

   ```sh
   userIdGeneratedByUser()
   'kcsy2
   SMFYb
   bWmeq
   ZXOYh
   2Rgxf
   '
   userIdGeneratedByUser()
   '1GCSgPLMaBAVQZ26
   YD7eFwNQKNs7qXaT
   ycArC5yrRupyG00S
   UbGxOFI7UXSWAyKN
   dIV0SSUTgAdKwStr
   '
   ```

2. Write a function **_generateColors_** which can generate any number of hexa or rgb colors.

   ```js
   console.log(generateColors("hexa", 3)); // ['#a3e12f', '#03ed55', '#eb3d2b']
   console.log(generateColors("hexa", 1)); // '#b334ef'
   console.log(generateColors("rgb", 3)); // ['rgb(5, 55, 175)', 'rgb(50, 105, 100)', 'rgb(15, 26, 80)']
   console.log(generateColors("rgb", 1)); // 'rgb(33,79, 176)'
   ```

3. Call your function _shuffleArray_, it takes an array as a parameter and it returns a shuffled array
4. Call your function _factorial_, it takes a whole number as a parameter and it return a factorial of the number
5. Call your function _isEmpty_, it takes a parameter and it checks if it is empty or not

6. Write a function called _average_, it takes an array parameter and returns the average of the items. Check if all the array items are number types. If not give return reasonable feedback.
