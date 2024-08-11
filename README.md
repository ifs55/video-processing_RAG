# video-processing_RAG

Ferramentas Utilizadas
Llama Index: Para criar índices multimodais.
OpenAI Whisper: Para transcrição de áudio.
LanceDB: Para armazenamento de vetores.
MoviePy: Para manipulação de vídeo.
PyTube: Para download de vídeos do YouTube.
SpeechRecognition: Para reconhecimento de fala.
ffmpeg-python: Para manipulação de áudio e vídeo.
Pillow: Para manipulação de imagens.
Matplotlib: Para visualização de imagens.
Processo de Implementação
1. Download do Vídeo
O vídeo é baixado do YouTube usando a biblioteca PyTube. A função download_video faz o download do vídeo na resolução mais alta disponível e salva os metadados do vídeo.
2. Extração de Frames do Vídeo
A função video_to_images extrai frames do vídeo a uma taxa de 0.2 fps e salva as imagens em um diretório especificado.
3. Extração de Áudio do Vídeo
A função video_to_audio extrai o áudio do vídeo e salva em um arquivo .wav.
4. Transcrição do Áudio para Texto
A função audio_to_text utiliza a biblioteca SpeechRecognition com o modelo OpenAI Whisper para transcrever o áudio em texto.
5. Indexação Multimodal
Os documentos de texto e imagens extraídas são carregados e indexados usando o MultiModalVectorStoreIndex do Llama Index. O armazenamento de vetores é feito utilizando o LanceDB.
6. Recuperação de Informações
O sistema é capaz de responder a consultas baseadas em texto e imagens. A função retrieve recupera informações relevantes do índice multimodal para responder às consultas.
7. Visualização de Imagens
A função plot_images visualiza até 5 imagens recuperadas da consulta.
Conclusão
O sistema  é capaz de processar vídeos para extrair frames, áudio e transcrever texto, além de indexar essas informações para recuperação eficiente. A integração de várias bibliotecas permite a criação de um pipeline robusto e eficiente para processamento e análise de vídeos, facilitando a recuperação de informações de maneira precisa e contextualizada.
