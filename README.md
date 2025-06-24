catalogo = Catalogo()

while True:
    print("1. Adicionar filme")
    print("2. Adicionar série")
    print("3. Adicionar jogo")
    print("4. Adicionar livro")
    print("5. Listar catálogo")
    print("6. Sair")

    escolha = input("Escolha uma opção: ")

    if escolha == "1":
        titulo = input("Título do filme: ")
        ano = int(input("Ano do filme: "))
        diretor = input("Diretor do filme: ")
        filme = Filme(titulo, ano, diretor)
        catalogo.adicionar(filme)
    elif escolha == "2":
        titulo = input("Título da série: ")
        ano = int(input("Ano da série: "))
        temporadas = int(input("Número de temporadas: "))
        serie = Serie(titulo, ano, temporadas)
        catalogo.adicionar(serie)
    elif escolha == "3":
        titulo = input("Título do jogo: ")
        ano = int(input("Ano do jogo: "))
        plataforma = input("Plataforma do jogo: ")
        jogo = Jogo(titulo, ano, plataforma)
        catalogo.adicionar(jogo)
    elif escolha == "4":
        titulo = input("Título do livro: ")
        ano = int(input("Ano do livro: "))
        autor = input("Autor do livro: ")
        livro = Livro(titulo, ano, autor)
        catalogo.adicionar(livro)
    elif escolha == "5":
        catalogo.listar()
    elif escolha == "6":
        break
    else:
        print("Opção inválida. Tente novamente.")
