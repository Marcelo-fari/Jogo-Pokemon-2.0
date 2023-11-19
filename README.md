# Jogo-Pokemon-2.0
Jogo Pokemon 2.0 EM Python


import random
print ("Bem Vindo A Arena Batalha Pokemon")


vida_inimigo =100
vida = 100


while  vida > 0  and vida_inimigo > 0:
    print ("Lista de ataques possíveis do Electabuzz")
    print ("1 - choque do trovão")
    print ("2 - soco de raios")
    print ("3 - trovão megamasterblaster")
    print ("4 - (SPECIAL)Voce usou raio supremo")


    ataque = input("Escolha qual ataque você quer usar: ")


    if ataque == "1":
         print ("Você usou o choque do trovão")
         vida_inimigo = vida_inimigo - 12
    elif ataque == "2":
         print ("Você usou soco de raios")
         vida_inimigo = vida_inimigo - 7
    elif ataque == "3":
         print("Você usou o trovão megamasterblaster")
         vida_inimigo = vida_inimigo - 18
    else:
         print ("(SPECIAL)Voce usou raio supremo")
         vida_inimigo = vida_inimigo - 50


    print("A vida do inimigo agora é", vida_inimigo)


    if vida_inimigo <= 0:
        break


    print("O chamander te ataca")
    ataque_inimigo_chance = random.randint(0,1)


    if ataque_inimigo_chance == 1:
        print("Chamander usa a bola de fogo")
        vida = vida - 15
    elif ataque_inimigo_chance == 2:
        print("Chamander usa cuspe de lava")
        vida = vida - 5
    else:
        print("chamander usa a arranhão")
        vida = vida - 8
    print("Sua vida agora é", vida,)


if vida > 0:
    print("Parabens, o Electabuzz Venceu")
else:
    print("Que Pena, o Chamander Venceu")
    print("Vai Voltar Chorando Pra Casa")
