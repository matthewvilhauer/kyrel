0. all_blue - [solution](/challenges/solutions/all_blue.js)

useBlue();
draw();
for(var i = 0; i < 4; i++) {
  moveRight();
  draw();
}

1. all_first_color - [solution](/challenges/solutions/all_first_color.js)

if (onBlue()) {
  useBlue();
} else if (onGreen()) {
  useGreen();
}
draw();
for(var i = 0; i < 4; i++) {
  moveRight();
  draw();
}

2. n_in_a_row - [solution](/challenges/solutions/n_in_a_row.js)

useBlue();
var number = 3;
draw();
for(var i = 0; i < number-1; i++) {
  moveRight();
  draw();
}

3. every_even_erase - [solution](/challenges/solutions/every_even_erase.js)

  start:  ['b', 'b', 'b', 'b', 'b']  
    finish: ['.', 'b', '.', 'b', '.']

    useBlue();

    for(var i = 0; i < 5; i++) {
      if (i % 2 === 0) {
        erase();
      }
      moveRight();
    }

4. every_odd_erase - [solution](/challenges/solutions/every_odd_erase.js)

  start:  ['b', 'b', 'b', 'b', 'b']  
    finish: ['b', '.', 'b', '.', 'b']  

    useBlue();

    for(var i = 0; i < 5; i++) {
      if (i % 2 != 0) {
        erase();
      }
      moveRight();
    }


5. every_n_erase - [solution](/challenges/solutions/every_n_erase.js)

  start:  ['b', 'b', 'b', 'b', 'b']  
  finish: ['.', '.', '.', '.', '.'] // (given n is 1)  
  finish: ['b', '.', 'b', '.', 'b'] // (given n is 2)   
  finish: ['b', 'b', 'b', 'b', '.'] // (given n is 5)  

  useBlue();
  n = 5;
  for(var i = 0; i < 5; i++) {

    for(var j = 0; j < n; j++) {
      moveRight();
    }
    erase();
  }

6. move_the_blue_dot_one_to_the_right - [solution](/challenges/solutions/move_the_blue_dot_one_to_the_right.js)

  start:  ['.', '.', 'b', '.', '.']  
    finish: ['.', '.', '.', 'b', '.']  

  start:  ['g', 'b', '.', '.', 'g']  
    finish: ['g', '.', 'b', '.', 'g']  



    useBlue();
    for (i = 0; i < 4; i++) {
      if (onBlue()) {
        erase();
        moveRight();
        draw();
        moveRight();
      } else {
        moveRight();
      }
    }

7. delete_before - [solution](/challenges/solutions/delete_before.js)

  start:  [ 'g', 'b', '.', '.', '.' ]    
  finish: [ '.', 'b', '.', '.', '.' ]    

  start:  [ 'g', 'b', 'b', '.', '.' ]    
  finish: [ '.', '.', 'b', '.', '.' ]
