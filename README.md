def calcular_media(notas):
    return sum(notas) / len(notas)


def verificar_situacao(media):
    if media >= 7:
        return "Aprovado"
    elif media >= 5:
        return "Recuperação"
    else:
        return "Reprovado"


def sistema():
    while True:
        print("\n=== Sistema de Alunos ===")
        print("1 - Cadastrar aluno")
        print("2 - Sair")

        opcao = input("Escolha uma opção: ")

        if opcao == "1":
            nome = input("Nome do aluno: ")

            notas = []
            for i in range(2):
                nota = float(input(f"Digite a nota {i+1}: "))
                notas.append(nota)

            media = calcular_media(notas)
            situacao = verificar_situacao(media)

            print("\n--- Resultado ---")
            print(f"Aluno: {nome}")
            print(f"Média: {media:.2f}")
            print(f"Situação: {situacao}")

        elif opcao == "2":
            print("Saindo do sistema...")
            break

        else:
            print("Opção inválida!")


sistema()
