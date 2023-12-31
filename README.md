# Padrões de projeto (Design Patterns)

# Singleton

## O que é?

Permite criar uma instância única de uma classe para todo o código. Independentemente de quantas vezes você instanciar um objeto desta classe. Ela sempre retornará a mesma instância.

Fornece um ponto de acesso global para essa instância.

## Utilidade

Permite encapsular atributos dessa classe, que serviriam como variáveis globais protegidas no código (não podem ser sobrescritas), a menos através dos métodos set.

## Código

``````python
# Exemplo de aplicação do Singleton na criação de uma conexão com um banco de dados
class DatabaseConnection:
    _instancia = None
    def __new__(cls):
        if not cls._instancia:
            cls._instancia = super(DatabaseConnection, cls).__new__(cls)
        return cls._instancia
        
    def read_data(self):
        # le o arquivo do banco de dados
        print('Lendo dados do banco de dados...')
    
    def write_data(self, dado):
        #escreve no arquivo do banco de dados
        print(f'Escrevendo no banco de dados: {dado}')
        
if __name__ == '__main__':
    c1 = DatabaseConnection()
    c2 = DatabaseConnection()
    
    c1.read_data()
    c2.write_data('novo dado')
``````

