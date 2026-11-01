# Compatibilidade do pacote — hardware-v1

| Item | Perfil atual |
|---|---|
| Sistema | Windows 11 x64, Intel/AMD; sem suporte homologado a Windows ARM. |
| Processador | x64 com AVX2; 6 núcleos ou mais recomendados. |
| RAM | Margem conservadora de 32 GB. Testes atuais em 96 GB; validação específica em 32 GB ainda pendente. |
| GPU | NVIDIA CUDA com 12 GB de VRAM dedicada ou mais; referência RTX 3060 12 GB. Driver compatível com CUDA 12.4. |
| Unidade dos modelos | NTFS/exFAT, 32 GB ou maior, 25 GiB livres no início da preparação. |
| Recomendação de unidade | 64 GB ou mais, USB 3.0; SSD externo para reduzir o tempo de carregamento. |
| Áudio | Microfone, saída de áudio e voz pt-BR instalada no Windows para usar a prática por voz. |
| Rede | Internet para preparação, ativação e verificações periódicas da licença. |

Os downloads somam **12.937.222.832 bytes = 12,937 GB = 12,049 GiB**.
Os pesos GGUF de geração/embeddings somam 12.099.763.872 bytes.
O instalador do aplicativo inclui Whisper; o preparador também o fixa para
compor o ambiente externo. A reserva de 25 GiB é uma margem operacional
para extração, temporários e preparação, não uma medição do tamanho final
de todos os documentos do usuário. GB é decimal; GiB é binário.

O perfil usa Qwen3.5 ou Ornith 9B, um por vez, com contexto configurado
de 32.768 tokens. A etapa de embeddings usa CPU. GPU de 12 GB é memória
dedicada, não memória compartilhada anunciada pelo Windows.

O processamento apenas em CPU, GPUs AMD/Intel e configurações abaixo
deste perfil **não foram homologados para esta distribuição**. A existência
de alternativa CPU no runtime não representa garantia de desempenho.
Resultados variam com o material e a carga do computador.

Uma mídia externa não transfere a ativação automaticamente para outro PC.
A conta admite uma instalação ativa. O uso offline é de até duas horas,
sempre limitado ao período contratado.

A confirmação destes requisitos no portal é registrada com o pedido.
Ela não afasta os direitos legais do consumidor.
