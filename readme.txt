-------------------------------------------Centro Universitário de Brasília---------------------------------------------------

-----------------------------------------------CIENCIA DA COMPUTAÇÃO---------------------------------------------------

-------------------------------------------SISTEMA EMBARCADO EM TEMPO REAL 1/2020---------------------------------------------------


DONO DO REPOSITORIO: https://github.com/igorgbs/python_face_reco

ABAIXO SEGUE O PASSO A PASSO PARA EXECUTAR


Primeiramente, é importante dizer que você deve possuir algum interpretador python instalado em sua máquina. Sugiro utilizar o Anaconda Python. Ele tem disponível para Windows, Mac e Linux. 

O Anaconda Python pode ser encontrado neste link:

https://www.anaconda.com/download/

Após instalar o Anaconda em sua máquina, deve instalar também o pacote pillow e opencv.

OpenCV: https://www.scivision.co/install-opencv-python-windows/
Pillow: https://wp.stolaf.edu/it/installing-pil-pillow-cimage-on-windows-and-mac/

Também é necessário que possua uma webcam em sua máquina.

1-Execute o arquivo Face_Capture_With_Rotate.py

Ao executar o código, abrirá uma tela com a imagem em tempo real da sua webcam. Em seguida, 50 fotos serão tiradas do seu rosto. Posicione o rosto o mais próximo do centro do quadrado que aparecerá na imagem. Após executar este arquivo, as 50 fotos que foram tiradas do seu rosto, ficarão armazenadas na pasta dataset e o seu nome e ID serão inseridos no arquivo Names.txt.

2- Após isso, execute o arquivo Trainner_All.py

Ao executar este arquivo, seu algoritmo será treinado para poder identificar as imagens posteriores. Ao fim da execução deste arquivo, 3 arquivos .xml serão adicionados ao diretório Recogniser. Estes arquivos conterão as informações necessárias para que seu algoritmo seja capaz de identificar os rostos.

3- Por fim, escolha um dos 3 algoritmos para reconhecimento: Recogniser_Video_EigenFace.py, Recogniser_Video_FisherFace.py ou Recogniser_Video_LBPH.py. 

Cada arquivo é responsável por utilizar um tipo diferente de algoritmo de reconhecimento. Execute os 3 e veja qual se sai melhor. 

É isso!

__________________________________________________________________________________________________________________________________


Detector_Video.py: Este arquivo detecta rostos usando cascatas Haar. Funciona bem com várias faces.

Face_Capture_With_Rotate.py: A execução desse arquivo captura 50 imagens de uma pessoa na frente da câmera. Isso garantirá que as fotos não sejam escuras e também fará com que o rosto fique reto.

Free_Rotate.py: Este arquivo mostra a função de rotação. Certifique-se de descomentar a linha 153 em NameFind.py. Isso mostrará a imagem corrigindo o deslocamento.

NameFind.py: Este arquivo contém todas as funções.

Trainer_All.py: Este arquivo treinará todos os algoritmos de reconhecimento usando as imagens na pasta dataSet.

Recogniser_Video_EigenFace.py: Este arquivo reconhece os rostos do feed da câmera usando o algoritmo de rosto Eigen.

Recogniser_video_FisherFace.py: Este arquivo é o que reconhecerá os rostos do feed da câmera usando o algoritmo de rosto de Fisher.

Recogniser_Video_LBPHFace.py: Este arquivo é o que reconhecerá os rostos do feed da câmera usando o algoritmo de rosto LBPH.

TestDataCollector_EiganFace.py: este arquivo é o aplicativo de teste. Será exibida uma imagem em que o conjunto de dados será carregado. Um loop será executado 200

vezes cada vez que aumenta o número de componentes. Cada vez que um reconhecedor de rosto Eigen será treinado e
previsto na imagem de entrada. Depois que o loop for for concluído, o ID e a confiança serão plotados.

TestDataCollector_EiganFace.py: este arquivo é o aplicativo de teste. Será exibida uma imagem em que o conjunto de dados será carregado. Um loop será executado 200

vezes cada vez que aumenta o número de componentes. Cada vez que um reconhecedor de rosto Fisher será treinado e
previsto na imagem de entrada. Depois que o loop for for concluído, o ID e a confiança serão plotados.

TestDataCollector_EiganFace.py: este arquivo é o aplicativo de teste. Será exibida uma imagem em que o conjunto de dados será carregado. Um loop será executado 54, 13, 50 vezes.

cada vez que aumenta os parâmetros. Cada vez que um reconhecedor de rosto LBPH será treinado e previsto na imagem de entrada.
Depois que o loop for for concluído, o ID e a confiança serão plotados.


------------------FOLDERS -----------
dataSet --> Contém as imagens que serão usadas para treinar o reconhecedor.
Haar --> Contém cascatas Haar de OpenCV usadas nas aplicações
Recogniser --> Contém os arquivos XML salvos pelos reconisadores
SaveData --> Contém os dados salvos pelos aplicativos testadores
