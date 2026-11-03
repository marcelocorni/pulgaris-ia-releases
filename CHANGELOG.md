# Pulgaris 0.15.0 — Windows x64

Aplicativo **0.15.0**, preparador **1.3.0**. Homologação concluída em **3 de novembro de 2026**.

## O que mudou

- Conferência semântica das avaliações e respostas, com checagem das partes explícitas da pergunta e citações verificadas.
- Recuperação documental com contexto adaptativo, trechos vizinhos e cache limitado; extração de PDFs por layout, tabelas alinhadas e OCR opcional em português pelo Windows.
- Operações com etapas, cancelamento e registro de interrupções; recuperação das respostas salvas sem reenvio automático.
- Backup consistente, cópia automática antes de migrações e restauração validada na próxima abertura, preservando a base anterior e o vínculo da instalação.
- Confirmação de e-mail e recuperação de senha no portal, com links de uso único e prazo de validade.
- Base para atualizações menores com manifesto assinado, integridade e reversão em caso de falha na verificação de saúde.
- Projetos com até 12 documentos, papéis, critérios por modalidade e acompanhamento qualitativo das sessões recentes.
- Verificação do ambiente e exportação de relatório de suporte sem documentos, respostas, áudio ou credenciais.

## Instalar ou atualizar

Feche o Pulgaris e instale **Pulgaris-0.15.0-Setup-win-x64.exe**. A biblioteca,
histórico, configurações e ativação existentes são preservados. Mantenha backup.
As versões anteriores à 0.15.0 devem usar o instalador completo; esta edição
inaugura o mecanismo de atualização menor para as próximas versões.

O preparador 1.3.0 e os modelos congelados permanecem compatíveis. Não é necessário
baixar os modelos novamente em um ambiente preparado e validado. O preparador
é pequeno; baixa e verifica runtime e modelos na unidade escolhida.

## Validação e limites

Foram aprovados **445 testes automatizados**, verificações nativas do pacote e
testes com Qwen e Ornith. A matriz final teve 13 casos sintéticos por modelo e
não registrou aprovações indevidas; houve avaliações inconclusivas. Isso não
representa uma taxa geral de acerto nem uma validação pedagógica humana.
A IA pode recusar uma avaliação sem segurança; confira as fontes.

O OCR depende do recurso de Português do Windows. Gemma continua experimental.
Os instaladores Inno Setup desta edição não possuem assinatura Authenticode.
O manifesto assinado de atualização é um mecanismo distinto dessa assinatura.

Leia **INSTALACAO.md** e **REQUISITOS.md**. Confira os arquivos em **SHA256SUMS.txt**.
Os modelos de voz homologados acompanham o aplicativo; modelos GGUF e llama.cpp
são obtidos pelo preparador. Os fontes permanecem no repositório privado.
