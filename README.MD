# Programação linear


Os problemas solucionados pela Programação Linear (PL) são problemas de otimização nos quais a função objetivo e as restrições são todas lineares.
A função objetivo é uma função matemática que contem uma ou mais variáveis de projeto que queremos otimizar.
Desejamos minimizar (e.g. o custo total de produção) ou maximizar (e.g. o lucro de venda) o valor da função objetivo.
As demais restrições do problema (e.g. capacidade de estocagem de cada produto, custo deste, tempo de reposição, etc) são expressas como funções também lineares.

Neste repositórios apresentamos quatro notebooks:

- 00-Introducao.ipynb
    + Mostramos uma introdução ao problema
    
- 01-Alocacao de recursos.ipynb
    + Mostramos como resolver um problema exemplo com programação linear
    
- 02-Alocacao inteira de recursos.ipynb
    + Acrescentamos uma restrição adicional ao problema, convertendo a um problema de programação linear inteira.

- 03-PuLP.ipynb
    + Este notebook utiliza uma outra biblioteca Python para resolver problemas de programação linear. Esta biblioteca permite selecionar diversos solver (métodos de resolução).


## Baixar este repositório

Você precisará ter o git instalado. Mais informações sobre a instalação do git [aqui](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git).


```
git clone https://github.com/h3dema/linear-programming.git
```

## Preparação do ambiente


Os comandos abaixo permitem a criação de um ambiente utilizando VENV para instalar as dependências para o python.
Estes comandos estão mostrados para um ambiente linux (eu utilizei um Ubuntu 18+).


```
cd linear-programming

python3 -m venv .venv
source .venv/bin/activate

pip3 install -r requirements.txt
```


### Instalando um solver

PuLP permite utilizar diversos solvers.
Vamos ver como utilizar [COIN-OR](https://github.com/coin-or/Clp) or [GLPK](https://www.gnu.org/software/glpk/), que são solvers free.

```
sudo apt-get install coinor-clp coinor-libclp-dev
sudo apt-get install coinor-cbc
sudo apt-get install glpk-utils
pulptest
```


Mais informações sobre a instalação podem ser encontradas [aqui](https://coin-or.github.io/user_introduction.html) (em inglês).
Os passos para instalar no Ubuntu podem ser encontrados [neste blog](https://ma.juii.net/blog/install-coin-or).