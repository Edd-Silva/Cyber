# Exemplos de uso do gerador de wordlist CEWL

## Extrair palavras-chave de um site e gerar uma wordlist:

cewl https://www.example.com -w wordlist.txt

## Definir o comprimento mínimo e máximo das palavras:

cewl https://www.example.com -w wordlist.txt --min_word_length 4 --max_word_length 10

## Limitar a profundidade da extração (número de links a seguir):

cewl https://www.example.com -w wordlist.txt --depth 2

## Excluir palavras comuns (stop words):

cewl https://www.example.com -w wordlist.txt --no-stop-words

## Salvar as palavras em ordem de frequência (mais frequentes primeiro):

cewl https://www.example.com -w wordlist.txt --count-sort

## Extrair palavras-chave de um arquivo local:

cewl file.html -w wordlist.txt

## Usar um arquivo de configuração personalizado:

cewl https://www.example.com -c myconfig.cfg -w wordlist.txt

## Gerar uma lista de palavras com base em um conjunto de caracteres:

cewl --charlist abcdefghijklmnopqrstuvwxyz0123456789 -m 4 -M 8 -w wordlist.txt

## Gerar uma lista de palavras com base em padrões comuns:

cewl --patterns "{word}{number}" -m 4 -M 8 -w wordlist.txt

## Gerar uma lista de palavras com base em um conjunto de prefixos e sufixos:

cewl --prefixes "pre" --suffixes "post" -m 4 -M 8 -w wordlist.txt

## Gerar uma lista de palavras com base em uma combinação de caracteres e padrões:

cewl --charlist abcdefghijklmnopqrstuvwxyz0123456789 --patterns "{char}{number}" -m 4 -M 8 -w wordlist.txt

## Gerar uma lista de palavras com base em uma lista personalizada de palavras:

cewl --wordlist custom_words.txt -m 4 -M 8 -w wordlist.txt

## Para criar um arquivo de texto separado contendo os nomes das pessoas, um nome por linha, e depois executar o CEWL especificando esse arquivo como a palavra-chave. Aqui está um exemplo de como fazer isso:

## Crie um arquivo chamado "nomes.txt" e insira os nomes das pessoas, um por linha:

João
Maria
Pedro
Ana

## Execute o CEWL com o arquivo "nomes.txt" como entrada:

cewl --wordlist wordlist.txt --dictionary nomes.txt

## Crie um arquivo chamado "nome.txt" e insira o nome da pessoa, juntamente com diferentes combinações de números e caracteres especiais:

Joao
Joao123
Jo@o
J0@0

## Execute o CEWL com o arquivo "nome.txt" como entrada:

cewl --wordlist wordlist.txt --dictionary nome.txt


## Isso instrui o CEWL a usar o arquivo "nome.txt" como dicionário para extrair palavras-chave e gerar a lista de palavras no arquivo "wordlist.txt".

Outros geradores de senhas

https://github.com/Mebus/cupp

Crunch

crunch 4 6 -t @@@@@ -o wordlist.txt

## Nesse exemplo, o Crunch irá gerar todas as combinações possíveis de palavras de 4 a 6 caracteres usando letras maiúsculas, minúsculas e dígitos. O resultado será salvo no arquivo "wordlist.txt".
