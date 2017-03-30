# Functional Programming Learning

## Attention

* pure function

* higher-order function

* Don't use iterate (eg: for、while etc)

  > we should use map、reduce、filter etc
  
* Avoid mutability
  
  > use immutable data

    ```
    // -> bad
    var rooms = ['h1', 'h2', 'h3'];
    rooms[2] = 'h4';
    rooms;
    // => ['h1', 'h2', 'h4']
    
    // -> good
    
    var rooms = ['h1', 'h2', 'h3'];

    var newRooms = rooms.map((item) => {
        if(item == 'h3') {
            return 'h4';
        } else {
            return item;
        }
    })

    newRooms;
    // => [ 'h1', 'h2', 'h4' ]
    rooms
    // => [ 'h1', 'h2', 'h3' ]
    ```
    
 * Presistent data structures for efficient immutability
  
  > Immutable.js
  
  
