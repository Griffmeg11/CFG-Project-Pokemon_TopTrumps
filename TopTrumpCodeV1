#random number
import random
import requests
import sys
pokemon_number_1 = random.randint(1,151)
url ='https://pokeapi.co/api/v2/pokemon/{}/'.format(pokemon_number_1)
response = requests.get(url)
pokemon1 = response.json()
print('\033[1;33;40mYour cards stats are:\n')
stats_1= [
    {"Name": "{}".format(pokemon1['name']) },
    {"Height": "{}".format(pokemon1['height']) },
    {"Weight": "{}".format(pokemon1['weight']) },
    {"ID": "{}".format(pokemon1['id']) },
    {"Experience":"{}".format(pokemon1['base_experience'])},
    {"Moves":"{}".format(pokemon1['order'])}
]
print("ID: {}".format(pokemon1['id']))
print("Name: {}".format(pokemon1['name']))
print("Height: {}".format(pokemon1['height']))
print("Weight: {}".format(pokemon1['weight']))
print("Experience: {}".format(pokemon1['base_experience']))
print("Moves: {}".format(pokemon1['order']))
# getting the second pokemon
pokemon_number_2 = random.randint(1,151)
url ='https://pokeapi.co/api/v2/pokemon/{}/'.format(pokemon_number_2)
response = requests.get(url)
pokemon2 = response.json()

stats_2= [
    {"Name": "{}".format(pokemon2['name']) },
    {"Height": "{}".format(pokemon2['height']) },
    {"Weight": "{}".format(pokemon2['weight']) },
    {"ID": "{}".format(pokemon2['id']) },
    {"Experience": "{}".format(pokemon2['base_experience']) },
    {"Moves": "{}".format(pokemon2['order']) }
]
while True:
    try:
        choice = input('Which stat do you want to use? Height/Weight/Experience/Moves: ')
        if choice == 'Height':
            us = (pokemon1['height'])
            them = (pokemon2['height'])
            break
        elif choice == 'Weight':
            us = (pokemon1['weight'])
            them = (pokemon2['weight'])
            break
        elif choice == 'Experience':
            us = (pokemon1['base_experience'])
            them = (pokemon2['base_experience'])
            break
        elif choice == 'Moves':
            us = (pokemon1['order'])
            them = (pokemon2['order'])
            break
        else:
            print('\033[1;31;40mPlease select from the 4 choices, careful with spelling and capitals\n')
    except ValueError:
        continue
print("You have selected {}".format(choice))

if us == them:
    print('Draw')
elif us > them:
    print('Winner')
elif us < them:
    print('Loser')

print("\033[1;33;40m\n")
Opponent = input("Do you want to see your opponents card?: y/n ")
if Opponent == 'y':
    print("\033[1;33;40m\n")
    print("ID: {}".format(pokemon2['id']))
    print("Your opponents stats were:")
    print("Name: {}".format(pokemon2['name']))
    print("Height: {}".format(pokemon2['height']))
    print("Weight: {}".format(pokemon2['weight']))
    print("Experience: {}".format(pokemon2['base_experience']))
    print("Moves: {}".format(pokemon2['order']))
else:
    print("You didn't want to see the opponents card")

sys.exit("Thanks for playing!")
