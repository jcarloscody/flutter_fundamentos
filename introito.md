
## ESTRUTURA DO FLUTTER
### FOLDERS
- `android:` proj nativo, o flutter encapsula toda a complexidade
do nativo, mas por debaixo do pano ele sempre executa o projeto 
nativo, quando subimos na lajas google/apple subimos o código nativo 
- `ios:` proj nativo
- `build:` o projeto compilado
- `lib:` onde ficará os arquivos dart que vc trabalha
- `test:` 

### FILES
- `pubspec.yaml:` toda a configuração do proj. 
   - `version:` versão dentro do proejto 
      - `1.0.0:` build name, nome da versão. Qual versão o projeto está.
      - `+1:` build number, toda vez que compilar um projeto para colocar na loja, deverá incrementar. é sequencial, sempre incrementar.
    - `enviroment:` versão do dart
    - `dependencies: `
    - `dev-dependencies:` dependências que apenas funcionam em tempo de desenvolvimento 
  
> `versão dos packages - `
>   `- significado do ^:` indica que vc quer a versão x, porém se houver atualização então deverá pegar esta última.
>  ` - numeração:`
>       `- 1º parte:` número absoluto, incompatível com a versão anterior
>       `- 2º parte:` indica novas features que não quebra a anterior
>       `- 3º parte:` a versão de bug fixed, indica correções
> 

> `versão transitivas:` as dependências que os packages usam.



## CANAIS DO FLUTTER
O Flutter trabalha com `canais` e este se subdivide em 4 canais que são eles os master, dev, beta, stable. ***comando: flutter channel*** 
É aconselhável trabalhar no canal da stabled
> - `stable:` canal que garante que as coisas não irão se quebrar. é onde se encontra o flutter estável. 
> - `beta:` está a versão que irá para a produção. será promovido para a stable.
> - `master:` é a branch principal de trabalho, onde a equipe está desenvolvendo.
> `dev:` canal em fase de falência, a partir da verão 2.8 não é mais atualizado, não será mais mantido pelo google.

- Comandos básicos
``` sh
- flutter --version
- flutter upgrade
- flutter upgrade
- flutter channel nome_canal
```

