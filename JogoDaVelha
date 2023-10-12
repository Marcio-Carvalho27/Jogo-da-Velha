import os

map = [["   ","   ","   "],["   ","   ","   "],["   ","   ","   "]]
c = 0
#dar print no mapa
def printMap(map):
    print(f"   0      1       2")
    print(f"0 {map[0][0]} |  {map[0][1]}  |  {map[0][2]}")
    print(f"   -      -       -")
    print(f"1 {map[1][0]} |  {map[1][1]}  |  {map[1][2]}")
    print(f"   -      -       -")
    print(f"2 {map[2][0]} |  {map[2][1]}  |  {map[2][2]}")

def printMapFinal(map):
    if verify(map) == 1:
        map[1][0] = map[1][1] = map[1][2] = map[2][0] = map[2][1] = map[2][2] = "   "
        printMap(map)
    elif verify(map) == 2:
        map[0][0] = map[0][1] = map[0][2] = map[2][0] = map[2][1] = map[2][2] = "   "
        printMap(map)
    elif verify(map) == 3:
        map[1][0] = map[1][1] = map[1][2] = map[0][0] = map[0][1] = map[0][2] = "   "
        printMap(map)
    elif verify(map) == 4:
        map[0][1] = map[1][1] = map[2][1] = map[0][2] = map[1][2] = map[2][2] = "   "
        printMap(map)
    elif verify(map) == 5:
        map[0][0] = map[1][0] = map[2][0] = map[0][2] = map[1][2] = map[2][2] = "   "
        printMap(map)
    elif verify(map) == 6:
        map[0][0] = map[1][0] = map[2][0] = map[0][1] = map[1][1] = map[2][1] = "   "
        printMap(map)
    elif verify(map) == 7:
        map[1][0] = map[2][0] = map[2][1] = map[0][1] = map[0][2] = map[1][2] = "   "
        printMap(map)
    elif verify(map) == 8:
        map[1][0] = map[0][0] = map[2][1] = map[0][1] = map[2][2] = map[1][2] = "   "
        printMap(map)

def verify(map):
    if map[0][0] == map[0][1] == map[0][2] != "   ":
        return 1
    elif map[1][0] == map[1][1] == map[1][2] != "   ":
        return 2
    elif map[2][0] == map[2][1] == map[2][2] != "   ":
        return 3
    elif map[0][0] == map[1][0] == map[2][0] != "   ":
        return 4
    elif map[0][1] == map[1][1] == map[2][1] != "   ":
        return 5
    elif map[0][2] == map[1][2] == map[2][2] != "   ":
        return 6
    elif map[0][0] == map[1][1] == map[2][2] != "   ":
        return 7
    elif map[2][0] == map[1][1] == map[0][2] != "   ":
        return 8
    else:
        return 9

#verifica se uma casa ja foi usada
def test(x, y):
    if map[x][y] == " X " or map[x][y] == " O ":
        return False
    else: 
        return True
    
def player(c):
    if c%2 == 0:
        print(f"\nVez do jogador -X- \nDigite 'linha coluna': ")
    else:
        print(f"\nVez do jogador -O- \nDigite 'linha coluna': ")

#jogar X e O
def main(map, c):
    while(9 == verify(map) and c != 9):
        printMap(map)
        player(c)
        x, y = input("").split()
        x = int(x)
        y = int(y)
        if test(x, y):
            if(c%2 == 0):
                p = " X "
                map[x][y] = p  
                c += 1
            else:
                p = " O "
                map[x][y] = p
                c += 1
        else:
            os.system("cls")
            print("Casa ja utilizada\n")
            main(map, c)
        os.system("cls")
        print(c)
        
    if c == 9 and verify(map) == 9:
        printMap(map)
        print("Deu velha")
    else:
        printMapFinal(map)
        print("\nParabens vc ganhou :)")
        

main(map, c)
