# Recursion..continued .. 

1. Recursion using parameters


 ## snippet
    def func(counter ): 
        if counter < 5:
            print("X")
            func(counter + 1)
    func(0)
### Recursion tree
![alt text](tree.jpg)


## Printing 1 to n (tail recursion)
![alt text](tail_visual.jpg)

        def func(n):
            if n==0:
                return
            func(n-1)
            print(n)
        func(5)



