# Instalação, atualização e uso — 0.14.1

## Instalar o aplicativo

Confira o SHA256 do instalador com o arquivo SHA256SUMS.txt da mesma release.
Feche o Pulgaris e instale **Pulgaris-0.14.1-Setup-win-x64.exe** sobre a instalação
atual. A biblioteca, histórico, preferências e ativação são preservados.
O pacote inclui .NET, Whisper Small/Base e Kokoro com Dora, Alex e Santa em pt-BR.

Ative em **Conta e ativação** com sua conta do portal e período válido.
A conta de administrador não recebe licença de uso automaticamente.
Uma instalação ativa por conta; até duas horas offline, limitadas à validade
do período contratado. Libere o vínculo no portal para trocar de computador.

## Preparar outro pen drive ou HD

1. Confira REQUISITOS.md e use NTFS ou exFAT.
2. Execute **Pulgaris-Preparador-1.3.0-Setup-win-x64.exe** e selecione uma
   **nova pasta**, por exemplo X:\Pulgaris-AI. Nenhuma unidade é formatada.
3. Abra **Preparar-Pulgaris.cmd**. Responda **S** para incluir Gemma experimental
   (+5,15 GB) ou **N** para manter Qwen, Ornith e embeddings.
4. O mesmo script baixa, confere SHA256 e prepara runtime, modelos e comandos.
   O requisito Microsoft pode pedir autorização do Windows. Nenhum modelo é
   iniciado ao concluir. Se houver interrupção, execute novamente para retomar.
5. Selecione essa pasta nas configurações do ambiente local do aplicativo.

Com Gemma, reserve 32 GiB livres em unidade de 64 GB ou maior.
A escolha é conservada para retomar uma preparação interrompida. Não substitua
manualmente pesos por versões de nome parecido nem use uma instalação de outro
projeto como destino do preparador.

Comandos individuais: Iniciar/Parar-Qwen35, Iniciar/Parar-Ornith,
Iniciar/Parar-Embeddings e, se incluído, Iniciar/Parar-Gemma4E4B.
Use somente um modelo por vez. Antes das operações do aplicativo, encerre os
servidores abertos manualmente; o Pulgaris preserva serviços preexistentes.

Um ambiente Pulgaris já preparado pode continuar sendo usado com Qwen e Ornith.
Para testar Gemma, selecione uma pasta que contenha a revisão congelada e seus
iniciadores. Os iniciadores experimentais previamente fornecidos são compatíveis;
não é preciso refazer esse ambiente se ele já contém o modelo conferido.

## Biblioteca, simulação e perguntas à IA

Importe o documento na Biblioteca e aguarde a indexação automática. Os controles
técnicos ficam no modo avançado. No Simulador, escolha documento, modalidade e
quantidade; o aplicativo prepara as N perguntas e apresenta uma por vez.

- Em **Avaliar a cada resposta**, envie a resposta e consulte a comparação,
  a resposta de referência e as fontes.
- Em **Responder tudo e avaliar ao final**, salve cada resposta e avance.
  Ao terminar, avalie todas.
- Se faltarem perguntas válidas, **Avaliar respostas salvas** permite encerrar
  e avaliar o que já foi respondido, sem recuperar pelo histórico.
- O roteiro e as respostas são salvos para retomada. A contagem planejada continua
  no relatório quando a sessão termina antes.
- Em **Perguntar à IA**, digite ou dite uma pergunta sobre o documento selecionado.

Qwen é padrão. Ative **Modo avançado** para escolher
**Gemma 4 E4B (experimental)** ou Ornith. A seleção das consultas é salva no perfil;
as simulações registram o modelo escolhido na sessão.

## Voz e teclado

Selecione microfone e saída em Áudio; as escolhas e o volume são salvos.
Whisper Small prioriza qualidade, e Base prioriza velocidade.
Revise a transcrição antes de enviá-la. A revisão opcional com IA mantém o original
e exige escolher Usar sugestão para substituir o texto.

Kokoro lê na saída escolhida, sem alterar o dispositivo padrão do Windows.
Em Preferências, ajuste voz, velocidade, pausas e pronúncia.
Novas perguntas podem ser lidas automaticamente; o botão permanece para repetir.
O microfone só é ligado por ação do usuário.

Atalhos são configuráveis em Preferências e funcionam com a janela em foco.
O padrão Ctrl+Shift+F6 salva e avança na avaliação ao final; Ctrl+Shift+F2 avalia
as respostas salvas quando a ação está disponível.

## Dicionários e números na leitura

Na Biblioteca, selecione o documento e abra **Pronúncia de…**. Clique em
**Sugerir com IA**, revise o rascunho e escolha **Salvar dicionário**. Novas
sugestões acrescentam termos ausentes e preservam suas correções. Também é
possível criar ou editar manualmente, no formato **Ethereum = Etéreum**.

No Simulador e em Perguntar à IA, **Usar pronúncias salvas deste documento**
aplica o dicionário correspondente; **Revisar dicionário** abre seu editor.
Sem dicionário específico, as pronúncias gerais de Preferências continuam em uso.
As entradas do documento têm prioridade, e as pronúncias numéricas automáticas
complementam os dois dicionários sem substituir os termos salvos.

Exemplos: **0,10244** vira zero vírgula um zero dois quatro quatro; **2 batatas**
vira duas batatas; datas completas, horários, moedas e porcentagens têm leitura
própria. Os textos da biblioteca, das perguntas e dos relatórios são preservados.
Datas inválidas ou formatos ambíguos não recebem uma interpretação inventada.

A barra animada indica o preparo. Ouvir novamente, pelo botão ou **Ctrl+Shift+F11**,
reutiliza o áudio compatível na saída atual. O cache fica somente em memória,
com limite de 16 áudios/64 MiB, e é limpo ao fechar o aplicativo. Mudanças no texto,
na voz, velocidade, pausas ou dicionário produzem novo áudio quando necessário.

## Verificação e limites

Os instaladores são Inno Setup e ainda não possuem assinatura digital comercial.
A release inclui hashes, changelog e instruções para conferência.
Gemma é experimental; quantidade de perguntas geradas e referências existentes
não garantem todas as interpretações da IA. Confira as fontes e compare com Qwen.
Preserve seus dados ao remover ou substituir uma pasta.
