# BaseXY

> Autor: @Ralfbp

---

## ✨ Desafio: Cryptografia

> Link: [https://ctf.chapeudepalhahacker.club/challenges#BaseXY-3](https://ctf.chapeudepalhahacker.club/challenges#BaseXY-3)

---

### Introdução

#### Enunciado

[![Captura-de-tela](https://i.postimg.cc/j5fD2wcN/Captura-de-tela-2025-06-06-134129.png)](https://postimg.cc/k6nJh5kX)

#### Mensagem criptografada

```
IZGECR33GBXDGX2QGEZWGM27OIZTI3DMPFPTG6BRORZSC7I=
```

#### 🛠️ Ferramenta utilizada:

```
https://www.dcode.fr/
```

#### A flag segue o seguinte padrão:

```
flag{.........}
```

---

## 🛠️ Resolução

1. Utilizando o site Dcode.

2. Na barra de pesquisa, procure por **Cipher Identifier**.

3. Na página correspondente, cole a mensagem criptografada na seção "Encrypted Message Identifier".

   [![Cipher Identifier](https://i.postimg.cc/jdVvcmFQ/Captura-de-tela-2025-06-06-134919.png)](https://postimg.cc/Hj2QsZHV)

4. O sistema identifica que é uma **string codificada em base32**.

5. Clique em **base32** para ser direcionado ao decodificador.

6. Cole a mensagem criptografada e a flag será revelada:

   [![Resultado base32](https://i.postimg.cc/8CCqGxDf/Captura-de-tela-2025-06-06-135126.png)](https://postimg.cc/ZW1fF7WJ)

```
FLAG{0n3_P13c3_r34lly_3x1ts!}
```

---

## ✅ Conclusão

O desafio BaseXY ensina a reconhecer e decodificar formatos comuns como o Base32, ferramenta essencial no mundo da criptografia.

> ⚡ A flag final é: **FLAG{0n3\_P13c3\_r34lly\_3x1ts!}**
