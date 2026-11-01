# Instalação e atualização

## Aplicativo

Instale `Pulgaris-<versão>-Setup-win-x64.exe` da release escolhida. O pacote
inclui o runtime .NET e o Whisper base homologado, com tamanho e hash
conferidos antes da transcrição. Para síntese, instale uma voz pt-BR pelo
Windows. O aplicativo não inclui uma voz neural ONNX.

Ative pela área **Conta e ativação** do aplicativo com os dados do portal.
Uma conta precisa de período válido e verificação para habilitar as
operações licenciadas. A conta de administrador não recebe licença de
uso automaticamente. A janela offline termina em até duas horas ou no
vencimento do plano, o que ocorrer primeiro.

## Preparar pen drive / HD

1. Confira [REQUISITOS.md](REQUISITOS.md), espaço e formato da unidade.
2. Abra o instalador do preparador e escolha uma **nova pasta vazia**,
   como `X:\Pulgaris-AI`. Não escolha a raiz nem uma instalação já existente.
3. Ao terminar, execute **Preparar-Pulgaris.cmd**. O script único baixa e
   confere todos os recursos fixados, instala o requisito Microsoft quando
   necessário e organiza modelos, runtime e controles. Não troca as versões
   por arquivos `latest`.
4. Se o download for interrompido, execute o mesmo script para retomá-lo.
   Nenhum arquivo com hash divergente é utilizado.
5. Informe essa pasta nas configurações de IA local do Pulgaris.

O resultado oferece seis controles:

- Iniciar / Parar Ornith;
- Iniciar / Parar Qwen35;
- Iniciar / Parar Embeddings.

Use um modelo por vez e pare antes de trocar. Pare também ao encerrar o
trabalho para liberar hardware. O preparador não inicia modelos sozinho.
O requisito Microsoft pode solicitar autorização do Windows; os modelos
e o runtime são obtidos pelo mesmo fluxo de preparação.

## Atualizações

Leia o changelog e as instruções da release antes de atualizar. Preserve
a biblioteca local e os dados da conta. Para um kit de IA com manifesto
diferente, prepare outra pasta e só então escolha a nova pasta no aplicativo.
Não sobrescreva manualmente pesos homologados por modelos de nome parecido.

O preparador não registra desinstalador para excluir seus modelos ou
documentos. Remover o aplicativo não deve ser usado para apagar a biblioteca.
Faça cópia dos seus dados antes de remover ou substituir uma pasta.

Para outro PC, libere a instalação ativa pelo portal antes de ativar a
nova. Uma confirmação offline anterior pode permanecer válida até o fim
da sua janela; a próxima consulta online aplica a liberação.
