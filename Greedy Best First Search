graph = {
    'P':[['A',4],['C',4],['R',4]],
    'A':[['M',3]],
    'C':[['M',6],['R',2],['U',3]],
    'R':[['E',5]],
    'M':[['L',2]],
    'U':[['S',4],['N',5]],
    'E':[['U',5],['S',1]],
    'N':[['S',6]],
    'S':[],
    'L':[['N',5]],
}
heus = {
    'P':10,
    'A':11,
    'C':6,
    'R':8,
    'M':9,
    'U':4,
    'E':3,
    'N':6,
    'S':0,
    'L':9
}
import math
current_node = 'P'
path = current_node
cost = 0
while current_node!='S':
    m = math.inf
    next_node = ''
    for child in graph[current_node]:
        if m>heus[child[0]]:
            next_node = child[0]
            m = heus[child[0]]
            current_cost = child[1]
    cost += current_cost
    current_node = next_node
    path += '-'+current_node
print(path,cost)
