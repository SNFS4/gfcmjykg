import random

#-------------------------------------------------------------------------
def BattleSystem(monsterType, playerHealth):
    if monsterType == "Creeper":
        monsterHealth = 20
        print("A creeper attacks!")
    elif monsterType == "Skeleton":
        monsterHealth = 40
        print("A skeleton attacks!")
        
    while monsterHealth>0 and playerHealth >0:
        if monsterType == "Creeper":
            monsterAttack = random.randrange(20, 30)
        elif monsterType == "Skeleton":
            monsterAttack = random.randrange(10, 16)
        print("The", monsterType, "attacks for", monsterAttack)
        playerHealth= playerHealth-monsterAttack
        print("Your health is now", playerHealth)
        
        playerAttack = random.randrange(25,35)
        print("You attack for", playerAttack)
        monsterHealth = monsterHealth - playerAttack
        print("The monster's health is now",monsterHealth)
        
    if monsterHealth<0:
        print("you win!")
    else:
        print("You Died")
    return playerHealth
#------------------------------------------------------------------------

while playerHealth>0 and choice != "quit":
BattleSystem("Skeleton", 100)
