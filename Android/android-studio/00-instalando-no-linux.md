# Instalando Android Studio no Linux

Abaixo vai um conjunto de passos genéricos e práticos para a instalação do `Android Studio` em distribuições Linux. Deixo claro que esta forma de instalação é uma preferência minha como desenvolvedor, após vários anos observando problemas de atualização e funcionamento em ambiente educacional. Caso tenha problemas durante a instalação, recomenda-se seguir a documentação original [aqui](https://developer.android.com/studio/install).

## Passos para instalação

1. Baixe a versão mais atual do `Android Studio`, clicando no botão `Download Android Studio...` na página: https://developer.android.com/studio

2. Aceite os termos para prosseguir com o download.

3. Um arquivo comprimido no formato `.tar.gz` será baixado para o seu computador na pasta de `Downloads` configurada para uso do seu navegador de preferêcia.

> OBS: Use o terminal linux para completar os passos seguintes.

4. Crie uma pasta onde ficará o `Android Studio` e os seus [SDKs](https://pt.wikipedia.org/wiki/Kit_de_desenvolvimento_de_software). Para isso, utilize o comando abaixo no terminal:

```bash
mkdir -p ~/Android
```

5. No terminal, vá até onde está o arquivo comprimido que contém o `Android Studio`. Aqui assumo que esteja dentro da pasta `Downloads`:

```bash
cd  ~/Downloads
```

6. Descomprima o conteúdo do arquivo `.tar.gz`:

```bash
tar -xvzf android-studio-*.tar.gz
```

7. Perceba que uma pasta `android-studio` será criada no diretório atual (`~/Downloads`) que você está. Se o comando abaixo não funcionar, provavelmente algo errado aconteceu durante a descompactação, ou uma pasta diferente foi criada durante o processo. Navegue até a sua pasta de **Downloads** para entender o que aconteceu.

```bash
ls -la android-studio
```

8. Mova a pasta `android-studio` para dentro do diretório `~/Android`.

```bash
mv android-studio ~/Android/android-studio
```

9. Faça a primeira execução da IDE para realizar a instalação. Apenas siga clicando em `Next`, porém atendando-se às informações disponibilizadas pela GUI de instalação. Para executar a partir do terminal, faça:

```bash
~/Android/android-studio/bin/studio
```

> OBS: após a instalação, para abrir o Android Studio você irá seguir para o caminho "Android/android-studio/bin/" que está na sua pasta home e depois dar dois cliques em "studio". Você pode criar um atalho amigável na próxima seção.

## Criando um atalho para a sua Área de Trabalho

Para criar um atalho de fácil acesso ao `Android Studio`, você deverá saber exatamente onde o instalou. Caso tenha seguido os passos da seção anterior (`~/Android/android-studio`), basta considerar que o caminho está na sua pasta `home` atual.

O comando abaixo assume que você irá criar um atalho para a sua `Área de Trabalho`:

```bash
ln -s /home/$USER/Android/android-studio/bin/studio /home/$USER/Área\ de\ Trabalho/Android\ Studio
```

> OBS: Caso queira iserir em outro local, considere alterar o parâmetro que segue logo após o espaço do caminho que leva ao executável `studio`.
