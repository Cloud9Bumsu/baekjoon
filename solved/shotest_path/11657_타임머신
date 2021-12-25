from copy import deepcopy

## initialize
N, M = map(int, input().split())
E = []

# distance  from 0
D = [float('inf') for n in range(N)]
D[0] = 0

# edge
for _ in range(M):
    E.append(list(map(int, input().split())))

###11656_타임머신 (벨만포드알고리즘)
## functions
def show_distance(D):
    print(D)

def edge_relaxation(u,v,w):
    if D[v-1] > D[u-1] + w:
        D[v-1] = D[u-1] + w

# main
def main():
    for i in range(N-1):
        for u,v,w in E:
            edge_relaxation(u,v,w)

    # negative cycle 
    D_ = deepcopy(D)
    for u,v,w in E:
        edge_relaxation(u,v,w)

    #show_distance(D)
    #show_distance(D_)
    
        
    if D_ != D:
        print('-1')
    else:
        for d in D[1:]:
            if d != float('inf'):
                print(d)
            else:
                print('-1')

main()
