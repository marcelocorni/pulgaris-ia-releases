# Pulgaris 0.15.1 — Windows x64

Aplicativo **0.15.1**, preparador **1.3.0**. Publicação autorizada em **3 de novembro de 2026**.

## Resolver o vínculo sem depender do suporte

- A mensagem explica que uma sessão anterior pode permanecer vinculada após reinstalar ou trocar de computador.
- Em Conta e ativação, **Liberar vínculo anterior…** abre uma confirmação dentro do aplicativo.
- Informe novamente a senha e escolha **Confirmar e ativar aqui**. O vínculo anterior é liberado e a instalação atual é ativada em uma única operação.
- Cancelar ou informar senha incorreta preserva a sessão anterior. Trocar o e-mail cancela a confirmação em aberto.
- Documentos, treinamentos, configurações e período contratado são preservados.
- A sessão anterior não pode renovar online. Uma confirmação offline já emitida permanece limitada ao seu prazo de até duas horas e à validade contratada.

## Atualizar

O instalador completo atualiza a instalação existente. Quem usa a 0.15.0 pode
optar pelo ZIP menor de código e seu manifesto assinado, conforme **ATUALIZACAO.md**.
A atualização do portal foi publicada junto com o aplicativo para habilitar o fluxo.
O preparador 1.3.0 e os modelos congelados permanecem iguais.

## Validação

**466 testes automatizados passaram**, incluindo confirmação, cancelamento,
senha incorreta, bloqueio por tentativas, revogação do token anterior,
preservação do período contratado e integração HTTP com banco isolado.
Os pacotes do aplicativo e do portal tiveram integridade conferida; o pacote
menor contém 420 arquivos de código, com assinatura verificada e sem modelos.

Confira **SHA256SUMS.txt**, **INSTALACAO.md** e **REQUISITOS.md**. Os instaladores
Inno Setup permanecem sem assinatura Authenticode comercial.
