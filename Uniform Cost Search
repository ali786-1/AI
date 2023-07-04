class Graph:
    def __init__(self):
        self.graph = {}
        n = int(input("Enter the number of nodes : "))
        alpha = "ABCDEFGHIJKLMNOPQRSTUVWXYZ"
        for i in range(n):
            c = int(input(f"Enter number of children of {alpha[i]} : "))
            self.graph[alpha[i]] = []
            for j in range(c):
                name = input("Enter the child node name : ")
                cost = int(input(f"Enter the cost to reach {name} from {alpha[i]} : "))
                self.graph[alpha[i]].append([name,cost])
    def UCS(self,start,goal):
        closed = []
        opened = [[start,0]]
        current_node = start
        current_cost = 0
        path = start
        while current_node != goal:
            for child in self.graph[current_node]:
                child[1] += current_cost
                opened.append(child)
            closed.append([current_node,current_cost])
            opened.remove([current_node,current_cost])
            opened.sort()
            m = 10000
            for node in opened:
                if node[1] < m:
                    m = node[1]
                    current_node = node[0]
                    current_cost = node[1]
            path += "-"+current_node
        print(path)
        print(current_cost)
