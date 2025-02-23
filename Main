lista_compras = []

def adicionar_item():
    try:
        nome = input("Digite o nome do produto: ")
        quantidade = int(input("Digite a quantidade: "))
        preco = float(input("Digite o preço unitário: "))
        lista_compras.append([nome, quantidade, preco])
        print(f"{nome} foi adicionado à lista de compras!")
    except ValueError:
        print("Erro: Quantidade e preço devem ser números. Tente novamente.")

def listar_itens():
    if not lista_compras:
        print("A lista de compras está vazia.")
    else:
        print("\nLista de Compras:")
        for i, item in enumerate(lista_compras, start=1):
            nome, quantidade, preco = item
            print(f"{i}. {nome} - {quantidade} unidades - R$ {preco:.2f} cada")

def calcular_total():
    try:
        total = sum(quantidade * preco for i, quantidade, preco in lista_compras)
        print(f"Total da lista de compras: R$ {total:.2f}")
    except Exception as e:
        print(f"Erro ao calcular o total: {e}")

def remover_item():
    try:
        listar_itens()
        if lista_compras:
            indice = int(input("Digite o número do item que deseja remover: ")) - 1
            if 0 <= indice < len(lista_compras):
                item_removido = lista_compras.pop(indice)
                print(f"{item_removido[0]} foi removido da lista de compras.")
            else:
                print("Número inválido!")
    except ValueError:
        print("Erro: Digite um número válido.")

while True:
    print("\n--- Lista de Compras ---")
    print("1. Adicionar item")
    print("2. Listar itens")
    print("3. Calcular total")
    print("4. Remover item")
    print("5. Sair")
    opcao = input("Escolha uma opção: ")

    if opcao == "1":
        adicionar_item()
    elif opcao == "2":
        listar_itens()
    elif opcao == "3":
        calcular_total()
    elif opcao == "4":
        remover_item()
    elif opcao == "5":
        print("Saindo...")
        break
    else:
        print("Opção inválida. Tente novamente.")
