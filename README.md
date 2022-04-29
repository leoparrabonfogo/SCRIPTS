# scripts

<details>
<summary>script teste</summary>

```bash
#!/bin/bash

variaveis do sistema
USER="Leo"
PASS="Senha"
VERMELHO="\033[31;1m"
VERDE="\033[32;1m"
AMARELO="\033[33;1m"
AZUL="\033[36;1m"
FECHAR="\033[m"

while :; do  
read -p "Login: " USER
read -p "Password: " PASS

if [[ "$USER" = "leo" ]] && [[ "$PASS" -eq "1234" ]]; then
    echo -e "${VERDE}Logado...Abrindo Menu"${FECHAR}
    break
    
else 
    echo -e ${VERMELHO}"Login invalido...Tente Novamente"${FECHAR}
    
fi
done
    sleep 1s

 echo -e ${AMARELO}"=======BEM VINDO======${FECHAR}
     ${AZUL}1) Abrir firefox${FECHAR}
     ${AZUL}2) Abrir Vs Code${FECHAR}
     ${AZUL}3) Abrir Calendario${FECHAR}
     ${AZUL}4) Abrir Calculadora${FECHAR}
     ${AZUL}5) Sair${FECHAR}
${AMARELO}======================${FECHAR}"

read -p "Selecione uma opcao: " OPCAO

case "$OPCAO" in
    1) firefox & ;;
    2) code & ;;
    3) calcurse & ;;
    4) galculator & ;;
    5) exit 0 & ;;
    *) echo "Essa opcao nao existe" ;;
esac
```
</details>
<br>


<details>
<summary>script 2</summary>

```bash
#!/bin/bash

list=("nome" "ddd" "telefone")

len="${#list[@]}"

declare -a completa
for (( i=0; i<$len; i++ )); do
  read -p "${list[$i]}: " line
  completa[$i]+=${line}
done

for i in $(seq 0 $len);
do
  echo "${list[$i]}: ${completa[$i]}"
done
```
</details>
<br>


