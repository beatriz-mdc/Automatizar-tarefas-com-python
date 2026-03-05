```python
import pyautogui
import time
```

- pyautogui.click -> clica
- pyautogui.write -> escreve um texto
- pyautogui.press -> aperta uma tecla
- pyautogui.hotkey -> aperta um atalho (hotkey)

***Passo 1: entrar no sistema da empresa***

***Abrir o navegador***
```python
pyautogui.PAUSE = 1
link = "https://dlp.hashtagtreinamentos.com/python/intensivao/login"
pyautogui.press("win")
pyautogui.write("chrome")
pyautogui.press("enter")
pyautogui.write(link)
pyautogui.press("enter")
```

***Fazer uma pausa maior para o site carregar***
```python
time.sleep(3)
```

***Passo 2: fazer login***

***Clicar no campo de email (verificar o arquivo auxiliar)***
```python
pyautogui.click(x=539, y=409)

pyautogui.write("pythonimpressionador@gmail.com")
pyautogui.press("tab")
pyautogui.write ("123456")
pyautogui.press("tab")
pyautogui.press("enter")
```

***Fazer uma pausa maior para o site carregar***
```python
time.sleep(3)
```

***Passo 3: abrir a base de dados (importar o arquivo)***
```python
import pandas

tabela = pandas.read_csv(r'C:\Users\14001071\Downloads\produtos.csv')
print(tabela)

for linha in tabela.index:
    ***Passo 4: cadastrar 1 produto***
    # código
    codigo = str(tabela.loc[linha, "codigo"])
    pyautogui.click(x=525, y=295) #clicar no campo do código
    pyautogui.write("MOLO000251")
    pyautogui.press("tab") #passar para o proximo campo
    # marca
    marca = str(tabela.loc[linha, "marca"])
    pyautogui.write("Logitech")
    pyautogui.press("tab")
    # tipo
    tipo = str(tabela.loc[linha, "tipo"])
    pyautogui.write("Mouse")
    pyautogui.press("tab")
    # categoria
    categoria = str(tabela.loc[linha, "categoria"])
    pyautogui.write(categoria)
    pyautogui.press("tab")
    # preço
    preco = str(tabela.loc[linha, "preco_unitario"])
    pyautogui.write(preco)
    pyautogui.press("tab")
    # custo
    custo = str(tabela.loc[linha, "custo"])
    pyautogui.write(custo)
    pyautogui.press("tab")
    # obs
    obs = str(tabela.loc[linha, "obs"])
    if obs != "nan":
        pyautogui.write(obs)
    pyautogui.press("tab") #passar para o botao enviar

pyautogui.press("enter")
```

***Voltar para o inicio da tela***
```python
pyautogui.scroll(5000)
```

***Passo 5: repetir o passo 4 até acabar a lista de produtos***






