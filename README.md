# Pulgaris — releases oficiais

Plataforma local de simulações, treinamento de comunicação e preparação oral
com o conhecimento do próprio usuário: **Academic, Interview, Oral e Present**.

**Versão atual: aplicativo 0.15.0 e preparador 1.3.0.**
Os instaladores, changelog e hashes estão na
[release v0.15.0](https://github.com/marcelocorni/pulgaris-ia-releases/releases/tag/v0.15.0).
Os fontes ficam em repositório privado. A licença do aplicativo é comercial;
dependências e modelos conservam suas respectivas licenças.

No [portal Pulgaris](https://pulgaris.com.br/#downloads), entre na sua conta
e use **Baixar aplicativo** ou **Baixar preparador**. Os botões redirecionam
diretamente aos arquivos oficiais; os instaladores ficam no GitHub.

## Escolher e instalar

| Arquivo | Finalidade |
|---|---|
| Pulgaris-0.15.0-Setup-win-x64.exe | Aplicativo Windows x64, runtime .NET, Whisper Small/Base e Kokoro pt-BR incluídos. |
| Pulgaris-Preparador-1.3.0-Setup-win-x64.exe | Assistente pequeno para preparar uma nova pasta no pen drive ou HD. Runtime e modelos são baixados depois. |
| SHA256SUMS.txt | Hashes dos arquivos desta release. |
| release.json | Versões e arquivos usados pelos links do portal. |

Leia [INSTALACAO.md](INSTALACAO.md) e [REQUISITOS.md](REQUISITOS.md).
Feche o aplicativo antes de atualizar sobre a instalação atual. A atualização
preserva biblioteca, histórico, configurações e ativação.

## Preparação e uso

1. Instale o aplicativo e ative em **Conta e ativação**, com sua conta e período válido.
2. Execute o preparador numa nova pasta da unidade escolhida, como X:\Pulgaris-AI.
3. Abra **Preparar-Pulgaris.cmd**. O mesmo script baixa, verifica e instala os
   componentes congelados. Responda **S** para incluir Gemma experimental ou **N**
   para manter o conjunto padrão de Qwen, Ornith e embeddings.
4. Selecione a pasta preparada no aplicativo e importe seu documento na Biblioteca.
   A indexação é automática.
5. No Simulador, escolha a modalidade e a quantidade. O roteiro é preparado
   antes e as perguntas são apresentadas uma por vez. É possível avaliar a cada
   resposta ou responder tudo antes da avaliação.
6. **Perguntar à IA** permite fazer suas próprias perguntas ao documento, com citações.

Os atalhos podem ser configurados em Preferências e funcionam com o Pulgaris em
foco. Microfone, saída e volume são salvos. A leitura automática de perguntas
pode ser desativada; o botão permite ouvi-las novamente.

## Pronúncia e repetição da voz

Na Biblioteca, cada documento pode ter seu dicionário de pronúncia. **Sugerir
com IA** acrescenta termos ao rascunho, preservando as correções existentes.
Revise e clique em **Salvar dicionário**. Simulação e Perguntar à IA usam as
pronúncias salvas do documento; elas têm prioridade sobre as gerais.

Números, datas, horários, valores e unidades usuais recebem pronúncias automáticas.
A parte decimal preserva todos os dígitos; quantidades usuais recebem concordância,
como **duas batatas** e **dois livros**. As regras complementam os dicionários e
respeitam correções manuais. Os textos originais permanecem intactos.

Uma barra indica o preparo da voz, inclusive pelo atalho **Ctrl+Shift+F11**.
Áudios prontos são reutilizados em memória (até 16 itens/64 MiB), usando saída e
volume atuais. Alterar texto, voz, velocidade, pausas ou dicionário exige áudio
compatível. Itens removidos do cache e a primeira leitura após fechar o aplicativo
precisam de novo preparo. A concordância usa regras para casos usuais; expressões
ambíguas podem receber correções no dicionário.

## Projetos, backup e diagnóstico

Em **Projetos e evolução**, reúna até 12 documentos com papéis como currículo,
vaga, critérios ou slides e escolha um material principal. O projeto pode ser
selecionado no Simulador e em Perguntar à IA. As sessões preservam as versões
utilizadas; a evolução é qualitativa e não representa uma nota oficial.

O menu de diagnóstico reúne **Salvar backup…**, **Restaurar um backup…**,
**Verificar meu ambiente** e exportação do relatório de suporte. O backup pode
incluir os originais e preserva biblioteca, pronúncias e treinamentos. A
restauração é aplicada ao reabrir, depois de guardar a base atual; a ativação
permanece vinculada ao computador. Guarde backups em local protegido.

A extração de PDFs considera layout e tabelas alinhadas. Em páginas digitalizadas,
o OCR opcional utiliza o recurso de Português do próprio Windows. Se esse recurso
não estiver disponível, o aplicativo informa a limitação.

As respostas passam por verificação de fontes e uma conferência semântica local.
Quando não há segurança para concluir, a avaliação fica inconclusiva. Confira
as fontes; perguntas com várias partes exigem resposta a todas elas.

A versão 0.15.0 inaugura a atualização de código com manifesto assinado.
Quem usa versões anteriores deve instalar o setup completo desta edição.
Os pacotes menores serão utilizados nas atualizações posteriores, preservando
os modelos de voz e os dados. A assinatura do manifesto não é assinatura
Authenticode do instalador; os EXEs desta edição continuam sem essa assinatura.

## Modelos e recursos congelados

| Componente | Versão | Bytes |
|---|---|---:|
| Qwen, padrão | 3.5 9B Q4_K_M | 5.680.522.464 |
| Ornith | 1.5 9B Q4_K_M | 5.780.090.816 |
| Gemma, opcional e experimental | 4 E4B IT QAT Q4_0 | 5.154.941.280 |
| Embeddings | Qwen3-Embedding 0.6B Q8_0 | 639.150.592 |
| Transcrição incluída no aplicativo | Whisper Small multilíngue | 487.601.967 |
| Transcrição rápida incluída | Whisper Base multilíngue | 147.951.465 |
| Síntese incluída | Kokoro 82M v1.0 FP32 ONNX | 325.508.342 |
| Vozes pt-BR incluídas | Dora, Alex e Santa | 522.368 por voz |
| Runtime externo de IA | llama.cpp b11853, CUDA 12.4 | Fixado pelo preparador |

Kokoro não exige vozes instaladas no Windows. Velocidade, pausas e dicionário
de pronúncia são configuráveis. Revisão textual da transcrição é opcional e
só substitui o texto após confirmação.

A preparação padrão baixa **12.937.222.832 bytes (~12,94 GB)**. Incluir Gemma
acrescenta **5.154.941.280 bytes**, totalizando **18.092.164.112 bytes (~18,09 GB)**.
O instalador pequeno não contém esses pesos. Revisões e SHA256 constam no
manifesto de modelos anexo à release; não se usam versões latest.

Qwen continua padrão. Gemma é uma opção experimental no modo avançado.
Granite não está incluído. Um modelo por vez, incluindo embeddings. O aplicativo
administra os serviços das operações; deixe servidores manuais encerrados.
Ao usar iniciadores diretamente, finalize pelo controle Parar correspondente.

## Requisitos e licença

Windows 11 x64, AVX2, 32 GB de RAM e GPU NVIDIA CUDA com 12 GB de VRAM dedicada
ou mais. CPU sem GPU, Windows ARM e GPUs AMD/Intel não são suportados.

Para o conjunto padrão: NTFS/exFAT, unidade de 32 GB ou maior e 25 GiB livres.
Com Gemma: unidade de 64 GB ou maior e **32 GiB livres** na preparação.
USB 3.0 é recomendado; FAT32 não comporta os modelos maiores que 4 GB.

Uma instalação ativa por conta. Ativação e verificações periódicas exigem
internet; uso offline de até duas horas, limitado ao período contratado.
Documentos e respostas permanecem locais. A avaliação é qualitativa:
confira as fontes; ela não equivale à nota de uma banca nem garante aprovação.

Contato e condições: [pulgaris.com.br](https://pulgaris.com.br).
Não publique senhas, documentos ou dados de pagamento em issues.
