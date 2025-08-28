# The Mentalists — Testes de API (Postman)

> **Projeto colaborativo** de testes de API desenvolvido em equipe durante o curso TQC - Qacoders 

---

## 📦 Conteúdo

* **Coleção Postman**: `The Mentalists.postman_collection.json`
* (Opcional) **Ambiente Postman**: `*.postman_environment.json`

---

## 🧭 Estrutura da Coleção

* **Auth**

  * Login Admin, validação de token e cenários de erro
* **User / CREATE**

  * Registro de usuário e validações de `fullName`, `mail`, `password` e `cpf`
* **User / UPDATE**

  * Alteração de `fullName`, `mail`, `password` e `status`
* **User / DELETE**

  * Exclusão de usuário (válido, inexistente, sem ID)
* **User / SELECT**

  * Listagem de usuários

---

## 🌐 Variáveis de Ambiente

| Variável     | Exemplo                        |
| ------------ | ------------------------------ |
| `url`        | `https://api.seudominio.com/`  |
| `mailAdmin`  | `admin@exemplo.com`            |
| `PassAdmin`  | `Secr3t@123`                   |
| `Mail`       | `qa.user@exemplo.com`          |
| `CPF`        | `12345678901`                  |
| `passUser`   | `1234@Test`                    |
| `tokenAdmin` | Gerado após login admin        |
| `IDUser`     | Gerado após criação de usuário |

---

## 🧪 Padrões de Teste

* **Status Code**: 200, 201, 400, 404, 409
* **Mensagens**: sucesso ou erro específicas
* **Persistência**: uso de variáveis de ambiente (`token`, `IDUser`, etc.)

---

## ▶️ Como Executar

### No Postman

1. Importar a coleção.
2. Criar ambiente e definir variáveis.
3. Rodar primeiro: **Auth > Login Admin**.
4. Depois: **User > CREATE**.
5. Em seguida, cenários de **UPDATE** e **DELETE**.

### Via Newman

```bash
newman run The\ Mentalists.postman_collection.json \
  -e ambiente.postman_environment.json \
  --reporters cli,htmlextra \
  --reporter-htmlextra-export reports/result.html
```

---

## 👥 Equipe

Este projeto foi desenvolvido em equipe durante o curso.

---

## 📄 Licença

Uso educacional. Adapte para seus estudos e portfólio.
