# Projetos-Python
Abaixo se encontra uma explicação breve do que cada parte do código está fazendo
  
# Verifica se `pergunta1` é um string vazio e também se ela é composta por apenas letras e espaços
        if pergunta1 == "" or all(nome.isalpha() for nome in pergunta1.split()):
            if pergunta1:
                print(f"Prazer te conhecer {pergunta1} !") # Se pergunta1 não for vazio, o código imprime a mensagem
            else:
                print("Não foi fornecido um nome...") # Se pergunta1 for vazio, ele retorna o loop
                continue

# Verifica se `pergunta2` é um valor entre 7 e 90 e então Imprime uma mensagem e encerra o loop
            pergunta2 = int(input(f"{pergunta1}, qual sua idade ?: "))
            if 7 <= pergunta2 <= 90:
                print(f"{pergunta2} anos ? Que legal {pergunta1} !") 
                break

# Caso `pergunta2` não tenha um valor entre 7 e 90, imprime a seguinte mensagem e encerra o loop
            else:
                print(f"{pergunta2} anos ? Acho que você está mentindo...")
                break
                
        else: # Caso pergunta1 não contenha apenas letras e espaços, ele retorna o loop
            print("Não foi fornecido um nome VÁLIDO...") 
            continue

# Caso ocorra um erro de valor na `pergunta2` - como uma string ao invés de integer - ele retorna o loop
    except ValueError:
        print("Erro... Por favor, insira um número válido para a idade.")
