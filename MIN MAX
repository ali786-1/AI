import math
terminals = [10,math.inf,5,-10,7,5,math.inf,-7,-5]
terminals
n = int(input("Enter how may layers : "))
for i in range(n):
    k = int(input("Enter number of nodes in this level : "))
    new_terminals = []
    for j in range(k):
        c = int(input("Enter how many children : "))
        if i%2==0:
            #min
            new_terminals.append(min(terminals[:c]))
        else:
            #max
            new_terminals.append(max(terminals[:c]))
        terminals = terminals[c:]
    terminals = new_terminals
print(terminals)
