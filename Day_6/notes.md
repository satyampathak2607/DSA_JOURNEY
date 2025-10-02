# Topic Covered:-

1. RECURSION


## SOME INSIGHTS 
      def greet():
        counter = 0
        print("Hello, World!")
        if counter <= 5: 
            ### DOESN'T WORKS
        
            greet()
            counter += 1
            return

### The counter is reset to 0 every time greet() is called, because it's a local variable inside the function. So it never reaches 5.

counter += 1 comes after the recursive call, which means it’s never actually executed in the recursion stack you're interested in.

## -> 
    def greet(counter=0): ### parameter ###
        print("Hello, World!")
        if counter < 5:
            greet(counter + 1)
    greet()

## IF U WANNA USE GLOBAL VARIABLE THEN YA NEED TO DEFINE IT

        count = 0
        def func():
            global count
            if count == 4:
                return
            print("saty")
            count += 1
            func()
        func()
        ''' we used global variable ...for it u need to declare it as global inside the function'''