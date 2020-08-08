import matplotlib.pyplot as plt
import numpy as np
from random import randint
#player_name="harry"
#player_attack=10
#player_heal=16
#health=100
# player=["manuel",10,16,100]

game_running=True
print("""        GAME INSTRUCTIONS
          ------------------------------------------
          *You and your opponent have 100 health each.
          *both of you have options to heal yourself or attack other alternatively one after other
          *your attack decreases 13 hp from your opponent
          *by healing your health will increase by 16
          *opponent's attack consumes 10 to 20 hp from your health
          *you have 10 choices to kill monster""")
#print(player["attack"])
while game_running==True:
    new_round=True
    counter=0
    player={"name":"harry","attack":13,"heal":16,"health":100}
    monster={"name":"voldemort","attack_min":10,"attack_max":20,"health":100}
    print("------"*4)
    print("enter player name")
    player["name"]=input()
    print(player["name"]+" has "+str(player["health"])+" health")
    print(monster["name"]+" has "+str(monster["health"])+" health")
    plt.style.use('ggplot')
    x = [player["name"], 'Voldemort']
    g = [player["health"],monster["health"]]
    x_pos = np.arange(len(x))
    plt.bar(x_pos, g, color='red')
    plt.xlabel("Players")
    plt.ylabel("Health")
    plt.xticks(x_pos, x)
    plt.axis([player["name"],'VOldemort',0,100])
    plt.show()
    
    while new_round==True:
        counter=counter +1
        player_won=False
        monster_won=False
        if counter<=10:
            
            
        
            print("------"*4)
            print("select action")
            print("1)attack")
            print("2)heal")
            print("3)exit")
            player_choice=int(input())
            monster_attack=randint(monster["attack_min"],monster["attack_max"])

            if player_choice==1:
                #print("attack")
                monster["health"]=monster["health"]-player["attack"]
                if monster["health"]>0:
                    player["health"]=player["health"]-monster_attack
                    if player["health"]>=0:
                        
                        print( monster["name"]+" has "+str(monster["health"])+" health left")
                        print(player["name"]+" has "+str(player["health"])+" health left")
                        print(player["name"]+" has "+str(10-counter)+"choices  more")
                        plt.style.use('ggplot')
                        x = [player["name"], 'Voldemort']
                        g = [player["health"],monster["health"]]
                        x_pos = np.arange(len(x))
                        plt.bar(x_pos, g, color='red')
                        plt.xlabel("Players")
                        plt.ylabel("Health")
                        plt.xticks(x_pos, x)
                        plt.axis([player["name"],'VOldemort',0,100])
                        plt.show()
                    else:
                        monster_won=True
                        print(monster["name"]+" won")
                        
                else:
                    player_won=True
                    print(player["name"]+" won")
                    
            elif player_choice==2:
                player["health"]=player["health"]+player["heal"]
                player["health"]=player["health"]-monster_attack
                if player["health"]<0:
                    monster_won=True
                    print(monster["name"]+" won")
                else:
                    print( monster["name"]+" has "+str(monster["health"])+" health  left")
                    print(player["name"]+" has "+str(player["health"])+" health left")
                    print(player["name"]+"has "+str(10-counter)+" choices more")
                    plt.style.use('ggplot')
                    x = [player["name"], 'Voldemort']
                    g = [player["health"],monster["health"]]
                    x_pos = np.arange(len(x))
                    plt.bar(x_pos, g, color='red')
                    plt.xlabel("Players")
                    plt.ylabel("Health")
                    plt.xticks(x_pos, x)
                    plt.axis([player["name"],'VOldemort',0,100])
                    plt.show()
                    
            elif player_choice==3:
                new_round=False
                game_running=False
            else :
                print("invalid input")
        elif counter>10:
             monster_won=True
             print(player["name"]+"has no more choices left and  "+monster["name"]+" won")
            
        if player_won== True or monster_won==True:
            new_round=False
            print("press 1 to restart the game")
            print("press 2 to exit the game")
            player_option=int(input())
            if player_option==1:
                game_running=True
            elif player_option==2:
                game_running=False
            
