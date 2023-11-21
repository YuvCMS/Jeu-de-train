print("------------------------------------------------------------------------")
print("---------------------\U0001F38A\U0001F4A5\U0001F4A5\U0001F4A5JEU DE TRAIN\U0001F4A5\U0001F4A5\U0001F4A5\U0001F38A-------------------")
print("------------------------------------------------------------------------")

print("Bienvenue à mon jeu !!! Ce jeu consiste à deviner un mot en ayant uniquement une seule lettre au début ! \n"
      "Si vous faites 5 erreurs,vous perdez la partie !!!\U000026D4\U000026D4\U000026D4\n"
      "les 5 wagons [˳˳_˳˳]--(˳˳_˳˳)--!˳˳X˳˳!--/˳˳_˳˳\--CRASH, representent les erreurs !!! \n"
      "\U0001F4D6Voyons voir si vous êtes un dictionnaire!!!\U0001F4D6\n "
      "Le joueur 1 \U0001F64B entre le mot et le joueur 2 \U0001F64B  continue le jeu.\n")
#je demande de rataper le mot pour une verification !! S'il se trompe , il doit recommencer le jeu
mot_1 = input("Joueur 1: Entrez le mot: ")
mot_2 = input("Joueur 1: Retapez le mot: ")
if mot_1 == mot_2:
     print("Merci \U0001F64F, passez à votre adversaire")
else :
     exit()

# Je crée une liste[] pour le mot entré pour separer les caracteres et je mesure aussi la longueur du mot.
list_mot_1=list(mot_1)
lenght=len(list_mot_1)

# Les commandes ci-dessous ont deux objectifs :
# -Afficher la première lettre du mot, ainsi que toutes les autres occurrences de cette lettre dans le mot, pour faciliter le jeu.
# -Remplacer les autres lettres par des tirets du bas.
# En effet, vu qu'on connaît la longueur du mot à deviner, j'utilise une boucle "for"
# pour que notre programme compare la première lettre du mot "[0]" avec les autres lettres.
# Si elle n'est pas identifiée, alors elle est remplacée par "_". Pour pouvoir le faire je crée une nouvelle liste "devine_mot"
# qui au debut contiendra rien et au fur est à mesure remplira les cases

devine_mot = [list_mot_1[0]]
for i in range (1, lenght):
     if(list_mot_1[0] == list_mot_1[i]):
          devine_mot.append(list_mot_1[0])
     else:
          devine_mot.append("_")

count_wrong = 0
memoire = [list_mot_1[0]]

while True:
     print("")
     print(devine_mot)

     lettre = input("Joueur 2: Entrez la lettre: ")

     if(lettre in memoire):
          print("Lettre déjà essayée, essaie une autre !")
     else:
          memoire.append(lettre)

          found = False
          for i in range(1, lenght):
               if list_mot_1[i] == lettre :
                    devine_mot[i] = lettre
                    found = True

          if(found==False):
               count_wrong = count_wrong + 1
               if(count_wrong == 1):
                    print("[˳˳_˳˳] \U000026A0\U000026A0\U000026A0")
               elif(count_wrong == 2):
                    print("[˳˳_˳˳]-(˳˳_˳˳) \U000026A0\U000026A0\U000026A0")
               elif(count_wrong == 3):
                    print ("[˳˳_˳˳]-(˳˳_˳˳)-!˳˳X˳˳! \U000026A0\U000026A0\U000026A0")
               elif(count_wrong == 4):
                    print("[˳˳_˳˳]-(˳˳_˳˳)-!˳˳X˳˳!-/˳˳_˳˳\\ \U000026A0\U000026A0\U000026A0")
               elif(count_wrong == 5):
                    print ("\U0001F4A3\U0001F4A3\U0001F4A3[˳˳_˳˳]-(˳˳_˳˳)-!˳˳X˳˳!-/˳˳_˳˳\\-*CRASH*\U0001F4A3\U0001F4A3\U0001F4A3")
                    print(" \U0001F44E \U0001F44E VOUS AVEZ PERDU \U0001F44E\U0001F44E\n")
                    print("Voici le mot: " + mot_1)
                    exit()
          else:
               print("BIEN DEVINÉ !!")
               if(not("_" in devine_mot)):
                    print("\U0001F3C6\U0001F3C6 VOUS AVEZ GAGNE !! \U0001F3C6\U0001F3C6\n" + "Voici le mot: " + mot_1)
                    exit()
