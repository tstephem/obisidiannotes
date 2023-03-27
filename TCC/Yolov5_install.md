# Yolov5 installation 

Para a podermos usar o yolov5 temos que passar por alguns procedimentos de instalação, primeiramente queremos instalar o Anaconda, a versão do CUDA que o pytorch usará( no meu caso cuda 11.6), CUDNN, o pytorch, pip e git no anaconda.

- Instalações no sistema
[Anaconda](https://www.anaconda.com/products/distribution)
[CUDA 11.6](https://developer.nvidia.com/cuda-11-6-0-download-archive)
[CUDNN](https://developer.nvidia.com/cudnn)

- Instalações no anaconda prompt

```conda
conda install pytorch torchvision torchaudio cudatoolkit=11.6 -c pytorch -c conda-forge
conda install -c anaconda pip
conda install -c anaconda git
```

- Clonando repositório do [Yolov5](https://github.com/ultralytics/yolov5)
```conda
git clone [https://github.com/ultralytics/yolov5](https://github.com/ultralytics/yolov5)  # clone
cd yolov5        # abrir a pasta
pip install -r requirements.txt      # instalar pacotes requeridos
```




