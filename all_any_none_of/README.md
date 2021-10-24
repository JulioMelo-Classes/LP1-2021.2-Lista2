# all_of, any_of e none_of

Implemente três funções all_of, any_of e none_of. Todas as três funções recebem um range \[first,last), um _predicado_ p. A função all_of retorna
verdadeiro quando o _predicado_ p é verdadeiro para __todos os elementos__ do range. A função any_of retorna true quando o _predicado_ p é verdadeiro
para __pelo menos um elemento__ do range. A função none_of retorna verdadeiro se o _predicado_ p é __falso para todos os elementos no range__.

As assinaturas das funções devem ser:
```c++
template <typename Itr , typename Predicate >
bool all_of ( Itr first , Itr last , Predicate p );
template <typename Itr , typename Predicate >
bool any_of ( Itr first , Itr last , Predicate p );
template <typename Itr , typename Predicate >
bool none_of ( Itr first , Itr last , Predicate p );
```

## Parâmetros
- first, last - os ponteiros apontando para o inicio e "fim" do range a ser considerado.
- p - uma função que retorna true quando uma determinada condição é satisfeita ou falso caso contrário.

Nest exercício o Predicado é uma função recebida por parâmetro, de forma que p possa ser usada como `p(*it1)`. Use essa função para
testar se um valor no range satisfaz o _predicado p_. Por exemlo, se você quer testar se o elemento apontado por it1 não satisfaz p
voce usaria ``!p(*it1)``.

## Retorno
- all_of: retorna verdadeiro se todos os elementos do range satisfazem p, falso caso contrário
- any_of: retorna verdadeiro se ao menos um elemento do range satisfaz p, falso caso contrário
- none_of: retorna verdadeiro se todos os elementos do range __não__ satisfazem p, falso caso contrário

## Executando os testes

Nesta questão para executar os testes você precisa fazer os seguintes comandos, no terminal, a partir do diretório onde este README está:

```
mkdir build
cd build
cmake ..
cmake --build . --target run_tests
```
