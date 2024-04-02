'''

dic = {
    'chave':'valor'
}
#print(dic['chave'])

dic['nova_chave'] = 'valor2'
print(dic)

dic['chave'] = 'outrovalor'
print(dic)

dic['chave'] = [dic['chave']] #transforma essa chave em lista
print(dic)
dic['chave'].append('valor3')#adicionando valor

#lopp nas chaves
print(dic.keys())#iteravel dá para dar loop

for key in dic.keys():
    print(f'{key} : {dic[key]}')#Acessando as chaves com o for



frase = 'Esta casa está ladrilhada, quem a desenladrilhará? O desenladrilhador. O desenladrilhador que a desenladrilhar, bom desenladrilhador será!'
print(frase)
frase = frase.lower()
print(frase)
for char in ',!?.':
    frase = frase.replace(char, '')
print(frase)
frase = frase.split(" ")
print(frase)
palavras = {}
for palavra in frase:
    if palavra not in palavras.keys():
        palavras[palavra] = 1
    else:
        palavras[palavra] += 1
print(palavras)

'''
'''#  C - CREATE / CRIA/CADASTRA
#  R - READ /   LER
#  U - UPDATE / ATUALIZA
#  D - DELETE / DELETA

peixes = {
    'Espécies' : ['Tilápia', "Baiacu", "Tucunaré", "Lambaqui", "Salmão", "Bacalhau", "Truta"],
    'Valor' : [25, 30, 20, 101, 45, 60,  15],
    'Região' : ["Piracicaba", "Oceania", "Amazonas", "aguas raras", "Noruega", "Portugal", "zona leste"],
    'estoque' : [10, 23, 3, 31, 42, 12, 21],
    'validade' : [9, 2, 10, 11, 7, 6, 3]
}

# Remover do estoque
indices = {peixes["Espécies"][i]: i for i in range(len(peixes["Espécies"]))}
def menu():
    opcao = input(f'O que você quer fazer : \n Cadastrar : {cadastrar()}  \n Informaçao : {infos()} \n Atualizar : {atualizar()}  \n Remover : {remover()}')
    if opcao == "Cadastrar":
        print(cadastrar())
    elif opcao == "Informaçao":
        print(infos())
    elif opcao == "Atualizar":
        print(atualizar())
    else:
        print(remover())

def obriga_opcao(lista,msg, msg_erro = None):
    resp = input(msg)
    while resp not in lista:
        print("Diga uma opção cadastrada!")
        if msg_erro:
            print(msg_erro)
        resp = input(msg)
    return resp


# cadastro de novo peixe

def cadastrar():
    for key in peixes.keys():
        info = input(f'Diga o/a novo/a {key}: ')
        peixes[key].append(info)
    return

def infos():
    qual = obriga_opcao(indices.keys(),"Qual peixe vc quer ver?",'\n'.join(peixes['Espécies']))
    indice = indices[qual]
    for key in peixes.keys():
        print(f"{key} : {peixes[key][indice]}")
    return
# atualizar

def atualizar():
    qual = obriga_opcao(indices.keys(),"Qual peixe vc quer atualizar?",'\n'.join(peixes['Espécies']))
    indice = indices[qual]
    for key in peixes.keys():
        peixes[key][indice] = input(f"Diga o novo {key}")
    return

def remover():
    peixe = obriga_opcao(indices.keys(),"Qual peixe vc quer remover?",'\n'.join(peixes['Espécies']))
    indice = indices[peixe]
    for key in peixes.keys():
        peixes[key].pop(indice)
    return

def menu():
   
while True:
    opcao = input(f'O que você quer fazer :  Cadastrar, Informaçao, Atualizar, Remover')
    if opcao == "Cadastrar":
        print(cadastrar())
    elif opcao == "Informaçao":
        print(infos())
    elif opcao == "Atualizar":
        print(atualizar())
    elif opcao == 'Remover':
        print(remover())
    else:
        print('Obrigado') 
    
infos()
menu()
'''

