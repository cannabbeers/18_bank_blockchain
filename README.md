# Bank blockchain - pychain
Module 18 Challenge

### Create a `blockchain` environment or modify your `dev` environment  to inclue all listed below:
        $ conda create -n blockchain -y -v -c conda-forge --strict-channel-priority ipykernel=6.24 jupyterlab=4.0 numpy=1.25 pandas=2.0 pip=23.1 python=3.11 python-dotenv=1.0 requests=2.31 streamlit=1.24 mnemonic=0.20

add following if not already installed: 

        conda install -c conda-forge web3
        conda install -c conda-forge watermark

        pip install eth-tester
        pip install bip44




### USAGE

Direct quote from starter code:

1. In the terminal, navigate to the project folder where you've coded the
  Challenge.

 2. In the terminal, run the Streamlit application by
using `streamlit run pychain.py`.

3. Enter values for the sender, receiver, and amount, and then click the "Add
Block" button. Do this several times to store several blocks in the ledger.

4. Verify the block contents and hashes in the Streamlit drop-down menu.
Take a screenshot of the Streamlit application page, which should detail a
blockchain that consists of multiple blocks. Include the screenshot in the
`README.md` file for your Challenge repository.

5. Test the blockchain validation process by using the web interface.
Take a screenshot of the Streamlit application page, which should indicate
the validity of the blockchain. Include the screenshot in the `README.md`
file for your Challenge repository. 

### GITBASH TERMINAL OUTPUT 

``` beers@hp_UCB_FT_2023 MINGW64 ~
$ conda activate blockchain
(blockchain)
beers@hp_UCB_FT_2023 MINGW64 ~
$ conda list
# packages in environment at C:\Users\beers\anaconda3\envs\blockchain:
#
# Name                    Version                   Build  Channel
aiohttp                   3.8.4           py311ha68e1ae_1    conda-forge
aiosignal                 1.3.1              pyhd8ed1ab_0    conda-forge
altair                    5.0.1              pyhd8ed1ab_1    conda-forge
anyio                     3.7.1              pyhd8ed1ab_0    conda-forge
argon2-cffi               21.3.0             pyhd8ed1ab_0    conda-forge
argon2-cffi-bindings      21.2.0          py311ha68e1ae_3    conda-forge
asn1crypto                1.5.1                    pypi_0    pypi
asttokens                 2.2.1              pyhd8ed1ab_0    conda-forge
async-lru                 2.0.3              pyhd8ed1ab_0    conda-forge
async-timeout             4.0.2              pyhd8ed1ab_0    conda-forge
attrs                     23.1.0             pyh71513ae_1    conda-forge
aws-c-auth                0.7.0                h6f3c987_2    conda-forge
aws-c-cal                 0.6.0                h6ba3258_0    conda-forge
aws-c-common              0.8.23               hcfcfb64_0    conda-forge
aws-c-compression         0.2.17               h420beca_1    conda-forge
aws-c-event-stream        0.3.1                had47b81_1    conda-forge
aws-c-http                0.7.11               h72ba615_0    conda-forge
aws-c-io                  0.13.28              ha35c040_0    conda-forge
aws-c-mqtt                0.8.14               h4941efa_2    conda-forge
aws-c-s3                  0.3.13               he04eaa7_2    conda-forge
aws-c-sdkutils            0.1.11               h420beca_1    conda-forge
aws-checksums             0.1.16               h420beca_1    conda-forge
aws-crt-cpp               0.20.3               h247a981_4    conda-forge
aws-sdk-cpp               1.10.57             h1a0519f_17    conda-forge
babel                     2.12.1             pyhd8ed1ab_1    conda-forge
backcall                  0.2.0              pyh9f0ad1d_0    conda-forge
backports                 1.0                pyhd8ed1ab_3    conda-forge
backports.functools_lru_cache 1.6.5              pyhd8ed1ab_0    conda-forge
base58                    2.1.1                    pypi_0    pypi
beautifulsoup4            4.12.2             pyha770c72_0    conda-forge
bip32                     3.4                      pypi_0    pypi
bip44                     0.1.3                    pypi_0    pypi
bitarray                  2.7.6           py311ha68e1ae_0    conda-forge
bleach                    6.0.0              pyhd8ed1ab_0    conda-forge
blinker                   1.6.2              pyhd8ed1ab_0    conda-forge
brotli-python             1.0.9           py311h12c1d0e_9    conda-forge
bzip2                     1.0.8                h8ffe710_4    conda-forge
c-ares                    1.19.1               hcfcfb64_0    conda-forge
ca-certificates           2023.5.7             h56e8100_0    conda-forge
cachetools                5.3.1              pyhd8ed1ab_0    conda-forge
certifi                   2023.5.7           pyhd8ed1ab_0    conda-forge
cffi                      1.15.1          py311h7d9ee11_3    conda-forge
charset-normalizer        3.2.0              pyhd8ed1ab_0    conda-forge
click                     8.1.6           win_pyh7428d3b_0    conda-forge
coincurve                 18.0.0                   pypi_0    pypi
colorama                  0.4.6              pyhd8ed1ab_0    conda-forge
comm                      0.1.3              pyhd8ed1ab_0    conda-forge
cytoolz                   0.12.0          py311ha68e1ae_1    conda-forge
debugpy                   1.6.7           py311h12c1d0e_0    conda-forge
decorator                 5.1.1              pyhd8ed1ab_0    conda-forge
defusedxml                0.7.1              pyhd8ed1ab_0    conda-forge
entrypoints               0.4                pyhd8ed1ab_0    conda-forge
eth-abi                   4.1.0              pyhd8ed1ab_0    conda-forge
eth-account               0.8.0              pyhd8ed1ab_1    conda-forge
eth-hash                  0.5.2              pyhd8ed1ab_0    conda-forge
eth-keyfile               0.6.1              pyhd8ed1ab_0    conda-forge
eth-keys                  0.4.0              pyhd8ed1ab_1    conda-forge
eth-rlp                   0.3.0              pyhd8ed1ab_0    conda-forge
eth-tester                0.9.0b2                  pypi_0    pypi
eth-typing                3.4.0              pyhd8ed1ab_0    conda-forge
eth-utils                 2.2.0           py311h1ea47a8_0    conda-forge
exceptiongroup            1.1.2              pyhd8ed1ab_0    conda-forge
executing                 1.2.0              pyhd8ed1ab_0    conda-forge
flit-core                 3.9.0              pyhd8ed1ab_0    conda-forge
freetype                  2.12.1               h546665d_1    conda-forge
frozenlist                1.4.0           py311ha68e1ae_0    conda-forge
gitdb                     4.0.10             pyhd8ed1ab_0    conda-forge
gitpython                 3.1.32             pyhd8ed1ab_0    conda-forge
hexbytes                  0.3.1              pyhd8ed1ab_0    conda-forge
idna                      3.4                pyhd8ed1ab_0    conda-forge
importlib-metadata        6.8.0              pyha770c72_0    conda-forge
importlib_metadata        6.8.0                hd8ed1ab_0    conda-forge
importlib_resources       6.0.0              pyhd8ed1ab_1    conda-forge
intel-openmp              2023.1.0         h57928b3_46319    conda-forge
ipykernel                 6.24.0             pyh6817e22_0    conda-forge
ipython                   8.14.0             pyh08f2357_0    conda-forge
ipywidgets                8.0.7              pyhd8ed1ab_0    conda-forge
jedi                      0.18.2             pyhd8ed1ab_0    conda-forge
jinja2                    3.1.2              pyhd8ed1ab_1    conda-forge
json5                     0.9.14             pyhd8ed1ab_0    conda-forge
jsonschema                4.18.4             pyhd8ed1ab_0    conda-forge
jsonschema-specifications 2023.7.1           pyhd8ed1ab_0    conda-forge
jupyter-lsp               2.2.0              pyhd8ed1ab_0    conda-forge
jupyter_client            8.3.0              pyhd8ed1ab_0    conda-forge
jupyter_core              5.3.1           py311h1ea47a8_0    conda-forge
jupyter_events            0.6.3              pyhd8ed1ab_0    conda-forge
jupyter_server            2.7.0              pyhd8ed1ab_0    conda-forge
jupyter_server_terminals  0.4.4              pyhd8ed1ab_1    conda-forge
jupyterlab                4.0.3              pyhd8ed1ab_0    conda-forge
jupyterlab_pygments       0.2.2              pyhd8ed1ab_0    conda-forge
jupyterlab_server         2.23.0             pyhd8ed1ab_0    conda-forge
jupyterlab_widgets        3.0.8              pyhd8ed1ab_0    conda-forge
krb5                      1.21.1               heb0366b_0    conda-forge
lcms2                     2.15                 h3e3b177_1    conda-forge
lerc                      4.0.0                h63175ca_0    conda-forge
libabseil                 20230125.3      cxx17_h63175ca_0    conda-forge
libarrow                  12.0.1           h0578746_5_cpu    conda-forge
libblas                   3.9.0              17_win64_mkl    conda-forge
libbrotlicommon           1.0.9                hcfcfb64_9    conda-forge
libbrotlidec              1.0.9                hcfcfb64_9    conda-forge
libbrotlienc              1.0.9                hcfcfb64_9    conda-forge
libcblas                  3.9.0              17_win64_mkl    conda-forge
libcrc32c                 1.1.2                h0e60522_0    conda-forge
libcurl                   8.2.0                hd5e4a3a_0    conda-forge
libdeflate                1.18                 hcfcfb64_0    conda-forge
libevent                  2.1.12               h3671451_1    conda-forge
libexpat                  2.5.0                h63175ca_1    conda-forge
libffi                    3.4.2                h8ffe710_5    conda-forge
libgoogle-cloud           2.12.0               hbc1b25b_1    conda-forge
libgrpc                   1.56.2               hea2d5f7_0    conda-forge
libhwloc                  2.9.1           nocuda_h15da153_6    conda-forge
libiconv                  1.17                 h8ffe710_0    conda-forge
libjpeg-turbo             2.1.5.1              hcfcfb64_0    conda-forge
liblapack                 3.9.0              17_win64_mkl    conda-forge
libpng                    1.6.39               h19919ed_0    conda-forge
libprotobuf               4.23.3               h1975477_0    conda-forge
libsodium                 1.0.18               h8d14728_1    conda-forge
libsqlite                 3.42.0               hcfcfb64_0    conda-forge
libssh2                   1.11.0               h7dfc565_0    conda-forge
libthrift                 0.18.1               h06f6336_2    conda-forge
libtiff                   4.5.1                h6c8260b_0    conda-forge
libutf8proc               2.8.0                h82a8f57_0    conda-forge
libwebp-base              1.3.1                hcfcfb64_0    conda-forge
libxcb                    1.15                 hcd874cb_0    conda-forge
libxml2                   2.11.4               hc3477c8_0    conda-forge
libzlib                   1.2.13               hcfcfb64_5    conda-forge
lru-dict                  1.2.0           py311ha68e1ae_0    conda-forge
lz4-c                     1.9.4                hcfcfb64_0    conda-forge
m2w64-gcc-libgfortran     5.3.0                         6    conda-forge
m2w64-gcc-libs            5.3.0                         7    conda-forge
m2w64-gcc-libs-core       5.3.0                         7    conda-forge
m2w64-gmp                 6.1.0                         2    conda-forge
m2w64-libwinpthread-git   5.0.0.4634.697f757               2    conda-forge
markdown-it-py            3.0.0              pyhd8ed1ab_0    conda-forge
markupsafe                2.1.3           py311ha68e1ae_0    conda-forge
matplotlib-inline         0.1.6              pyhd8ed1ab_0    conda-forge
mdurl                     0.1.0              pyhd8ed1ab_0    conda-forge
mistune                   3.0.0              pyhd8ed1ab_0    conda-forge
mkl                       2022.1.0           h6a75c08_874    conda-forge
mnemonic                  0.20               pyhd8ed1ab_0    conda-forge
msys2-conda-epoch         20160418                      1    conda-forge
multidict                 6.0.4           py311ha68e1ae_0    conda-forge
nbclient                  0.8.0              pyhd8ed1ab_0    conda-forge
nbconvert-core            7.7.1              pyhd8ed1ab_1    conda-forge
nbformat                  5.9.1              pyhd8ed1ab_0    conda-forge
nest-asyncio              1.5.6              pyhd8ed1ab_0    conda-forge
notebook-shim             0.2.3              pyhd8ed1ab_0    conda-forge
numpy                     1.25.1          py311h0b4df5a_0    conda-forge
openjpeg                  2.5.0                ha2aaf27_2    conda-forge
openssl                   3.1.1                hcfcfb64_1    conda-forge
orc                       1.9.0                hf2b8f0d_1    conda-forge
overrides                 7.3.1              pyhd8ed1ab_0    conda-forge
packaging                 23.1               pyhd8ed1ab_0    conda-forge
pandas                    2.0.3           py311hf63dbb6_1    conda-forge
pandocfilters             1.5.0              pyhd8ed1ab_0    conda-forge
parsimonious              0.9.0              pyhd8ed1ab_0    conda-forge
parso                     0.8.3              pyhd8ed1ab_0    conda-forge
pbkdf2                    1.3                pyhd8ed1ab_0    conda-forge
pickleshare               0.7.5                   py_1003    conda-forge
pillow                    9.5.0           py311hde623f7_1    conda-forge
pip                       23.1.2             pyhd8ed1ab_0    conda-forge
pkgutil-resolve-name      1.3.10             pyhd8ed1ab_0    conda-forge
platformdirs              3.9.1              pyhd8ed1ab_0    conda-forge
prometheus_client         0.17.1             pyhd8ed1ab_0    conda-forge
prompt-toolkit            3.0.39             pyha770c72_0    conda-forge
prompt_toolkit            3.0.39               hd8ed1ab_0    conda-forge
protobuf                  4.23.3          py311h03b55d4_0    conda-forge
psutil                    5.9.5           py311ha68e1ae_0    conda-forge
pthread-stubs             0.4               hcd874cb_1001    conda-forge
pthreads-win32            2.9.1                hfa6e2cd_3    conda-forge
pure_eval                 0.2.2              pyhd8ed1ab_0    conda-forge
pyarrow                   12.0.1          py311h6a6099b_5_cpu    conda-forge
pycparser                 2.21               pyhd8ed1ab_0    conda-forge
pycryptodome              3.18.0          py311ha68e1ae_0    conda-forge
pydeck                    0.8.0              pyhd8ed1ab_0    conda-forge
pygments                  2.15.1             pyhd8ed1ab_0    conda-forge
pympler                   1.0.1              pyhd8ed1ab_0    conda-forge
pysocks                   1.7.1              pyh0701188_6    conda-forge
python                    3.11.4          h2628c8c_0_cpython    conda-forge
python-dateutil           2.8.2              pyhd8ed1ab_0    conda-forge
python-dotenv             1.0.0              pyhd8ed1ab_0    conda-forge
python-fastjsonschema     2.17.1             pyhd8ed1ab_0    conda-forge
python-json-logger        2.0.7              pyhd8ed1ab_0    conda-forge
python-tzdata             2023.3             pyhd8ed1ab_0    conda-forge
python_abi                3.11                    3_cp311    conda-forge
pytz                      2023.3             pyhd8ed1ab_0    conda-forge
pytz-deprecation-shim     0.1.0.post0     py311h1ea47a8_3    conda-forge
pywin32                   304             py311h12c1d0e_2    conda-forge
pywinpty                  2.0.11          py311h12c1d0e_0    conda-forge
pyyaml                    6.0             py311ha68e1ae_5    conda-forge
pyzmq                     25.1.0          py311h7b3f143_0    conda-forge
re2                       2023.03.02           hd4eee63_0    conda-forge
referencing               0.30.0             pyhd8ed1ab_0    conda-forge
regex                     2023.6.3        py311ha68e1ae_0    conda-forge
requests                  2.31.0             pyhd8ed1ab_0    conda-forge
rfc3339-validator         0.1.4              pyhd8ed1ab_0    conda-forge
rfc3986-validator         0.1.1              pyh9f0ad1d_0    conda-forge
rich                      13.4.2             pyhd8ed1ab_0    conda-forge
rlp                       3.0.0              pyhd8ed1ab_0    conda-forge
rpds-py                   0.9.2           py311hc37eb10_0    conda-forge
semantic-version          2.10.0                   pypi_0    pypi
send2trash                1.8.2              pyh08f2357_0    conda-forge
setuptools                68.0.0             pyhd8ed1ab_0    conda-forge
six                       1.16.0             pyh6c4a22f_0    conda-forge
smmap                     3.0.5              pyh44b312d_0    conda-forge
snappy                    1.1.10               hfb803bf_0    conda-forge
sniffio                   1.3.0              pyhd8ed1ab_0    conda-forge
soupsieve                 2.3.2.post1        pyhd8ed1ab_0    conda-forge
stack_data                0.6.2              pyhd8ed1ab_0    conda-forge
streamlit                 1.24.1             pyhd8ed1ab_1    conda-forge
tbb                       2021.9.0             h91493d7_0    conda-forge
tenacity                  8.2.2              pyhd8ed1ab_0    conda-forge
terminado                 0.17.0             pyh08f2357_0    conda-forge
tinycss2                  1.2.1              pyhd8ed1ab_0    conda-forge
tk                        8.6.12               h8ffe710_0    conda-forge
toml                      0.10.2             pyhd8ed1ab_0    conda-forge
tomli                     2.0.1              pyhd8ed1ab_0    conda-forge
toolz                     0.12.0             pyhd8ed1ab_0    conda-forge
tornado                   6.3.2           py311ha68e1ae_0    conda-forge
traitlets                 5.9.0              pyhd8ed1ab_0    conda-forge
typing-extensions         4.7.1                hd8ed1ab_0    conda-forge
typing_extensions         4.7.1              pyha770c72_0    conda-forge
typing_utils              0.1.0              pyhd8ed1ab_0    conda-forge
tzdata                    2023c                h71feb2d_0    conda-forge
tzlocal                   4.3             py311h1ea47a8_0    conda-forge
ucrt                      10.0.22621.0         h57928b3_0    conda-forge
urllib3                   2.0.4              pyhd8ed1ab_0    conda-forge
validators                0.20.0             pyhd8ed1ab_0    conda-forge
vc                        14.3                h64f974e_17    conda-forge
vc14_runtime              14.36.32532         hfdfe4a8_17    conda-forge
vs2015_runtime            14.36.32532         h05e6639_17    conda-forge
watchdog                  3.0.0           py311h1ea47a8_0    conda-forge
watermark                 2.4.3              pyhd8ed1ab_0    conda-forge
wcwidth                   0.2.6              pyhd8ed1ab_0    conda-forge
web3                      6.5.0           py311h1ea47a8_0    conda-forge
webencodings              0.5.1                      py_1    conda-forge
websocket-client          1.6.1              pyhd8ed1ab_0    conda-forge
websockets                11.0.3          py311ha68e1ae_0    conda-forge
wheel                     0.40.0             pyhd8ed1ab_1    conda-forge
widgetsnbextension        4.0.8              pyhd8ed1ab_0    conda-forge
win_inet_pton             1.1.0              pyhd8ed1ab_6    conda-forge
winpty                    0.4.3                         4    conda-forge
xorg-libxau               1.0.11               hcd874cb_0    conda-forge
xorg-libxdmcp             1.1.3                hcd874cb_0    conda-forge
xz                        5.2.6                h8d14728_0    conda-forge
yaml                      0.2.5                h8ffe710_2    conda-forge
yarl                      1.9.2           py311ha68e1ae_0    conda-forge
zeromq                    4.3.4                h0e60522_1    conda-forge
zipp                      3.16.2             pyhd8ed1ab_0    conda-forge
zstd                      1.5.2                h12be248_7    conda-forge
(blockchain)
beers@hp_UCB_FT_2023 MINGW64 ~
$ cd Desktop/
(blockchain)
beers@hp_UCB_FT_2023 MINGW64 ~/Desktop
$ cd HW_repos/
(blockchain)
beers@hp_UCB_FT_2023 MINGW64 ~/Desktop/HW_repos
$ git clone https://github.com/cannabbeers/18_bank_blockchain.git
Cloning into '18_bank_blockchain'...
remote: Enumerating objects: 14, done.
remote: Counting objects: 100% (14/14), done.
remote: Compressing objects: 100% (13/13), done.
remote: Total 14 (delta 4), reused 0 (delta 0), pack-reused 0
Receiving objects: 100% (14/14), 7.36 KiB | 1.84 MiB/s, done.
Resolving deltas: 100% (4/4), done.
(blockchain)
beers@hp_UCB_FT_2023 MINGW64 ~/Desktop/HW_repos
$ code .
(blockchain)
beers@hp_UCB_FT_2023 MINGW64 ~/Desktop/HW_repos
$ cd 18_bank_blockchain/
(blockchain)
beers@hp_UCB_FT_2023 MINGW64 ~/Desktop/HW_repos/18_bank_blockchain (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   pychain.py

no changes added to commit (use "git add" and/or "git commit -a")
(blockchain)
beers@hp_UCB_FT_2023 MINGW64 ~/Desktop/HW_repos/18_bank_blockchain (main)
$ git add .
(blockchain)
beers@hp_UCB_FT_2023 MINGW64 ~/Desktop/HW_repos/18_bank_blockchain (main)
$ git commit -m "saving progress, finished step 1-2, starting 3 next"
[main b691550] saving progress, finished step 1-2, starting 3 next
 1 file changed, 20 insertions(+), 6 deletions(-)
(blockchain)
beers@hp_UCB_FT_2023 MINGW64 ~/Desktop/HW_repos/18_bank_blockchain (main)
$ git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 759 bytes | 759.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/cannabbeers/18_bank_blockchain.git
   854eb4f..b691550  main -> main
(blockchain)
beers@hp_UCB_FT_2023 MINGW64 ~/Desktop/HW_repos/18_bank_blockchain (main)
$ git add .
(blockchain)
beers@hp_UCB_FT_2023 MINGW64 ~/Desktop/HW_repos/18_bank_blockchain (main)
$ git commit -m "ready to test in streamlit"
[main 874b9d4] ready to test in streamlit
 1 file changed, 25 insertions(+), 11 deletions(-)
(blockchain)
beers@hp_UCB_FT_2023 MINGW64 ~/Desktop/HW_repos/18_bank_blockchain (main)
$ git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 938 bytes | 938.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/cannabbeers/18_bank_blockchain.git
   b691550..874b9d4  main -> main
(blockchain)
beers@hp_UCB_FT_2023 MINGW64 ~/Desktop/HW_repos/18_bank_blockchain (main)
$ streamlit run pychain.py

  You can now view your Streamlit app in your browser.

  Local URL: http://localhost:8501
  Network URL: http://10.0.0.241:8501

Last updated: 2023-07-19T15:56:39.847490-07:00

Python implementation: CPython
Python version       : 3.11.4
IPython version      : 8.14.0

Compiler    : MSC v.1935 64 bit (AMD64)
OS          : Windows
Release     : 10
Machine     : AMD64
Processor   : Intel64 Family 6 Model 154 Stepping 4, GenuineIntel
CPU cores   : 12
Architecture: 64bit

pandas   : 2.0.3
streamlit: 1.24.1

Initializing Chain
2023-07-19 15:56:40.043 `st.cache` is deprecated. Please use one of Streamlit's new caching commands,
`st.cache_data` or `st.cache_resource`.

More information [in our docs](https://docs.streamlit.io/library/advanced-features/caching).
Last updated: 2023-07-19T15:56:58.352775-07:00

Python implementation: CPython
Python version       : 3.11.4
IPython version      : 8.14.0

Compiler    : MSC v.1935 64 bit (AMD64)
OS          : Windows
Release     : 10
Machine     : AMD64
Processor   : Intel64 Family 6 Model 154 Stepping 4, GenuineIntel
CPU cores   : 12
Architecture: 64bit

pandas   : 2.0.3
streamlit: 1.24.1

2023-07-19 15:56:58.369 `st.cache` is deprecated. Please use one of Streamlit's new caching commands,
`st.cache_data` or `st.cache_resource`.

More information [in our docs](https://docs.streamlit.io/library/advanced-features/caching).
Last updated: 2023-07-19T15:57:10.015710-07:00

Python implementation: CPython
Python version       : 3.11.4
IPython version      : 8.14.0

Compiler    : MSC v.1935 64 bit (AMD64)
OS          : Windows
Release     : 10
Machine     : AMD64
Processor   : Intel64 Family 6 Model 154 Stepping 4, GenuineIntel
CPU cores   : 12
Architecture: 64bit

pandas   : 2.0.3
streamlit: 1.24.1

2023-07-19 15:57:10.024 `st.cache` is deprecated. Please use one of Streamlit's new caching commands,
`st.cache_data` or `st.cache_resource`.

More information [in our docs](https://docs.streamlit.io/library/advanced-features/caching).
Last updated: 2023-07-19T15:57:26.558229-07:00

Python implementation: CPython
Python version       : 3.11.4
IPython version      : 8.14.0

Compiler    : MSC v.1935 64 bit (AMD64)
OS          : Windows
Release     : 10
Machine     : AMD64
Processor   : Intel64 Family 6 Model 154 Stepping 4, GenuineIntel
CPU cores   : 12
Architecture: 64bit

pandas   : 2.0.3
streamlit: 1.24.1

2023-07-19 15:57:26.574 `st.cache` is deprecated. Please use one of Streamlit's new caching commands,
`st.cache_data` or `st.cache_resource`.

More information [in our docs](https://docs.streamlit.io/library/advanced-features/caching).
Last updated: 2023-07-19T15:57:29.122272-07:00

Python implementation: CPython
Python version       : 3.11.4
IPython version      : 8.14.0

Compiler    : MSC v.1935 64 bit (AMD64)
OS          : Windows
Release     : 10
Machine     : AMD64
Processor   : Intel64 Family 6 Model 154 Stepping 4, GenuineIntel
CPU cores   : 12
Architecture: 64bit

pandas   : 2.0.3
streamlit: 1.24.1

2023-07-19 15:57:29.136 `st.cache` is deprecated. Please use one of Streamlit's new caching commands,
`st.cache_data` or `st.cache_resource`.

More information [in our docs](https://docs.streamlit.io/library/advanced-features/caching).
Wining Hash 00f49e81d6bbc61446a08152c7c93e9613944d435f27251b1446fae959fdf746
Last updated: 2023-07-19T15:58:07.860846-07:00

Python implementation: CPython
Python version       : 3.11.4
IPython version      : 8.14.0

Compiler    : MSC v.1935 64 bit (AMD64)
OS          : Windows
Release     : 10
Machine     : AMD64
Processor   : Intel64 Family 6 Model 154 Stepping 4, GenuineIntel
CPU cores   : 12
Architecture: 64bit

pandas   : 2.0.3
streamlit: 1.24.1

2023-07-19 15:58:07.878 `st.cache` is deprecated. Please use one of Streamlit's new caching commands,
`st.cache_data` or `st.cache_resource`.

More information [in our docs](https://docs.streamlit.io/library/advanced-features/caching).
Last updated: 2023-07-19T15:58:08.279229-07:00

Python implementation: CPython
Python version       : 3.11.4
IPython version      : 8.14.0

Compiler    : MSC v.1935 64 bit (AMD64)
OS          : Windows
Release     : 10
Machine     : AMD64
Processor   : Intel64 Family 6 Model 154 Stepping 4, GenuineIntel
CPU cores   : 12
Architecture: 64bit

pandas   : 2.0.3
streamlit: 1.24.1

2023-07-19 15:58:08.294 `st.cache` is deprecated. Please use one of Streamlit's new caching commands,
`st.cache_data` or `st.cache_resource`.

More information [in our docs](https://docs.streamlit.io/library/advanced-features/caching).
Last updated: 2023-07-19T15:58:23.814177-07:00

Python implementation: CPython
Python version       : 3.11.4
IPython version      : 8.14.0

Compiler    : MSC v.1935 64 bit (AMD64)
OS          : Windows
Release     : 10
Machine     : AMD64
Processor   : Intel64 Family 6 Model 154 Stepping 4, GenuineIntel
CPU cores   : 12
Architecture: 64bit

pandas   : 2.0.3
streamlit: 1.24.1

2023-07-19 15:58:23.829 `st.cache` is deprecated. Please use one of Streamlit's new caching commands,
`st.cache_data` or `st.cache_resource`.

More information [in our docs](https://docs.streamlit.io/library/advanced-features/caching).
Last updated: 2023-07-19T15:58:23.971890-07:00

Python implementation: CPython
Python version       : 3.11.4
IPython version      : 8.14.0

Compiler    : MSC v.1935 64 bit (AMD64)
OS          : Windows
Release     : 10
Machine     : AMD64
Processor   : Intel64 Family 6 Model 154 Stepping 4, GenuineIntel
CPU cores   : 12
Architecture: 64bit

pandas   : 2.0.3
streamlit: 1.24.1

2023-07-19 15:58:23.992 `st.cache` is deprecated. Please use one of Streamlit's new caching commands,
`st.cache_data` or `st.cache_resource`.

More information [in our docs](https://docs.streamlit.io/library/advanced-features/caching).
Last updated: 2023-07-19T15:58:25.534823-07:00

Python implementation: CPython
Python version       : 3.11.4
IPython version      : 8.14.0

Compiler    : MSC v.1935 64 bit (AMD64)
OS          : Windows
Release     : 10
Machine     : AMD64
Processor   : Intel64 Family 6 Model 154 Stepping 4, GenuineIntel
CPU cores   : 12
Architecture: 64bit

pandas   : 2.0.3
streamlit: 1.24.1

2023-07-19 15:58:25.549 `st.cache` is deprecated. Please use one of Streamlit's new caching commands,
`st.cache_data` or `st.cache_resource`.

More information [in our docs](https://docs.streamlit.io/library/advanced-features/caching).
Last updated: 2023-07-19T15:58:26.502984-07:00

Python implementation: CPython
Python version       : 3.11.4
IPython version      : 8.14.0

Compiler    : MSC v.1935 64 bit (AMD64)
OS          : Windows
Release     : 10
Machine     : AMD64
Processor   : Intel64 Family 6 Model 154 Stepping 4, GenuineIntel
CPU cores   : 12
Architecture: 64bit

pandas   : 2.0.3
streamlit: 1.24.1

2023-07-19 15:58:26.519 `st.cache` is deprecated. Please use one of Streamlit's new caching commands,
`st.cache_data` or `st.cache_resource`.

More information [in our docs](https://docs.streamlit.io/library/advanced-features/caching).
Last updated: 2023-07-19T15:58:28.090167-07:00

Python implementation: CPython
Python version       : 3.11.4
IPython version      : 8.14.0

Compiler    : MSC v.1935 64 bit (AMD64)
OS          : Windows
Release     : 10
Machine     : AMD64
Processor   : Intel64 Family 6 Model 154 Stepping 4, GenuineIntel
CPU cores   : 12
Architecture: 64bit

pandas   : 2.0.3
streamlit: 1.24.1

2023-07-19 15:58:28.106 `st.cache` is deprecated. Please use one of Streamlit's new caching commands,
`st.cache_data` or `st.cache_resource`.

More information [in our docs](https://docs.streamlit.io/library/advanced-features/caching).
Wining Hash 0000bdc952e20319b3d839ff26012e2ab6ea35c6d79cef036d52e73dd76350e5
Last updated: 2023-07-19T15:58:36.415387-07:00

Python implementation: CPython
Python version       : 3.11.4
IPython version      : 8.14.0

Compiler    : MSC v.1935 64 bit (AMD64)
OS          : Windows
Release     : 10
Machine     : AMD64
Processor   : Intel64 Family 6 Model 154 Stepping 4, GenuineIntel
CPU cores   : 12
Architecture: 64bit

pandas   : 2.0.3
streamlit: 1.24.1

2023-07-19 15:58:36.428 `st.cache` is deprecated. Please use one of Streamlit's new caching commands,
`st.cache_data` or `st.cache_resource`.

More information [in our docs](https://docs.streamlit.io/library/advanced-features/caching).
Last updated: 2023-07-19T15:58:36.666989-07:00

Python implementation: CPython
Python version       : 3.11.4
IPython version      : 8.14.0

Compiler    : MSC v.1935 64 bit (AMD64)
OS          : Windows
Release     : 10
Machine     : AMD64
Processor   : Intel64 Family 6 Model 154 Stepping 4, GenuineIntel
CPU cores   : 12
Architecture: 64bit

pandas   : 2.0.3
streamlit: 1.24.1

2023-07-19 15:58:36.666 `st.cache` is deprecated. Please use one of Streamlit's new caching commands,
`st.cache_data` or `st.cache_resource`.

More information [in our docs](https://docs.streamlit.io/library/advanced-features/caching).
Last updated: 2023-07-19T15:59:07.982912-07:00

Python implementation: CPython
Python version       : 3.11.4
IPython version      : 8.14.0

Compiler    : MSC v.1935 64 bit (AMD64)
OS          : Windows
Release     : 10
Machine     : AMD64
Processor   : Intel64 Family 6 Model 154 Stepping 4, GenuineIntel
CPU cores   : 12
Architecture: 64bit

pandas   : 2.0.3
streamlit: 1.24.1

2023-07-19 15:59:08.000 `st.cache` is deprecated. Please use one of Streamlit's new caching commands,
`st.cache_data` or `st.cache_resource`.

More information [in our docs](https://docs.streamlit.io/library/advanced-features/caching).
Last updated: 2023-07-19T15:59:23.303358-07:00

Python implementation: CPython
Python version       : 3.11.4
IPython version      : 8.14.0

Compiler    : MSC v.1935 64 bit (AMD64)
OS          : Windows
Release     : 10
Machine     : AMD64
Processor   : Intel64 Family 6 Model 154 Stepping 4, GenuineIntel
CPU cores   : 12
Architecture: 64bit

pandas   : 2.0.3
streamlit: 1.24.1

2023-07-19 15:59:23.308 `st.cache` is deprecated. Please use one of Streamlit's new caching commands,
`st.cache_data` or `st.cache_resource`.

More information [in our docs](https://docs.streamlit.io/library/advanced-features/caching).
Last updated: 2023-07-19T15:59:29.489747-07:00

Python implementation: CPython
Python version       : 3.11.4
IPython version      : 8.14.0

Compiler    : MSC v.1935 64 bit (AMD64)
OS          : Windows
Release     : 10
Machine     : AMD64
Processor   : Intel64 Family 6 Model 154 Stepping 4, GenuineIntel
CPU cores   : 12
Architecture: 64bit

pandas   : 2.0.3
streamlit: 1.24.1

2023-07-19 15:59:29.505 `st.cache` is deprecated. Please use one of Streamlit's new caching commands,
`st.cache_data` or `st.cache_resource`.

More information [in our docs](https://docs.streamlit.io/library/advanced-features/caching).
Last updated: 2023-07-19T15:59:29.623814-07:00

Python implementation: CPython
Python version       : 3.11.4
IPython version      : 8.14.0

Compiler    : MSC v.1935 64 bit (AMD64)
OS          : Windows
Release     : 10
Machine     : AMD64
Processor   : Intel64 Family 6 Model 154 Stepping 4, GenuineIntel
CPU cores   : 12
Architecture: 64bit

pandas   : 2.0.3
streamlit: 1.24.1

2023-07-19 15:59:29.643 `st.cache` is deprecated. Please use one of Streamlit's new caching commands,
`st.cache_data` or `st.cache_resource`.

More information [in our docs](https://docs.streamlit.io/library/advanced-features/caching).
Last updated: 2023-07-19T15:59:32.480943-07:00

Python implementation: CPython
Python version       : 3.11.4
IPython version      : 8.14.0

Compiler    : MSC v.1935 64 bit (AMD64)
OS          : Windows
Release     : 10
Machine     : AMD64
Processor   : Intel64 Family 6 Model 154 Stepping 4, GenuineIntel
CPU cores   : 12
Architecture: 64bit

pandas   : 2.0.3
streamlit: 1.24.1

2023-07-19 15:59:34.171 `st.cache` is deprecated. Please use one of Streamlit's new caching commands,
`st.cache_data` or `st.cache_resource`.

More information [in our docs](https://docs.streamlit.io/library/advanced-features/caching).
Wining Hash 000007d882768e7d20879ab871f1737480628291ed228b36cd8e2d550840d63e
Wining Hash 00000df9654c75a1ef071171eaa4206ca9985bdc441fb343bcdebdf1ec154ddf
Blockchain is invalid!
Last updated: 2023-07-19T16:00:10.333604-07:00

Python implementation: CPython
Python version       : 3.11.4
IPython version      : 8.14.0

Compiler    : MSC v.1935 64 bit (AMD64)
OS          : Windows
Release     : 10
Machine     : AMD64
Processor   : Intel64 Family 6 Model 154 Stepping 4, GenuineIntel
CPU cores   : 12
Architecture: 64bit

pandas   : 2.0.3
streamlit: 1.24.1

2023-07-19 16:00:10.351 `st.cache` is deprecated. Please use one of Streamlit's new caching commands,
`st.cache_data` or `st.cache_resource`.

More information [in our docs](https://docs.streamlit.io/library/advanced-features/caching).
Wining Hash 00000fa8e27de46ea371cd9bfd4dfe37282f1eb76ae825329788f3918f79791a
Last updated: 2023-07-19T16:00:17.381995-07:00

Python implementation: CPython
Python version       : 3.11.4
IPython version      : 8.14.0

Compiler    : MSC v.1935 64 bit (AMD64)
OS          : Windows
Release     : 10
Machine     : AMD64
Processor   : Intel64 Family 6 Model 154 Stepping 4, GenuineIntel
CPU cores   : 12
Architecture: 64bit

pandas   : 2.0.3
streamlit: 1.24.1

2023-07-19 16:00:17.397 `st.cache` is deprecated. Please use one of Streamlit's new caching commands,
`st.cache_data` or `st.cache_resource`.

More information [in our docs](https://docs.streamlit.io/library/advanced-features/caching).
Last updated: 2023-07-19T16:00:31.832465-07:00

Python implementation: CPython
Python version       : 3.11.4
IPython version      : 8.14.0

Compiler    : MSC v.1935 64 bit (AMD64)
OS          : Windows
Release     : 10
Machine     : AMD64
Processor   : Intel64 Family 6 Model 154 Stepping 4, GenuineIntel
CPU cores   : 12
Architecture: 64bit

pandas   : 2.0.3
streamlit: 1.24.1

2023-07-19 16:00:31.889 `st.cache` is deprecated. Please use one of Streamlit's new caching commands,
`st.cache_data` or `st.cache_resource`.

More information [in our docs](https://docs.streamlit.io/library/advanced-features/caching).
Last updated: 2023-07-19T16:00:45.040586-07:00

Python implementation: CPython
Python version       : 3.11.4
IPython version      : 8.14.0

Compiler    : MSC v.1935 64 bit (AMD64)
OS          : Windows
Release     : 10
Machine     : AMD64
Processor   : Intel64 Family 6 Model 154 Stepping 4, GenuineIntel
CPU cores   : 12
Architecture: 64bit

pandas   : 2.0.3
streamlit: 1.24.1

2023-07-19 16:00:45.057 `st.cache` is deprecated. Please use one of Streamlit's new caching commands,
`st.cache_data` or `st.cache_resource`.

More information [in our docs](https://docs.streamlit.io/library/advanced-features/caching).
Last updated: 2023-07-19T16:01:03.603525-07:00

Python implementation: CPython
Python version       : 3.11.4
IPython version      : 8.14.0

Compiler    : MSC v.1935 64 bit (AMD64)
OS          : Windows
Release     : 10
Machine     : AMD64
Processor   : Intel64 Family 6 Model 154 Stepping 4, GenuineIntel
CPU cores   : 12
Architecture: 64bit

pandas   : 2.0.3
streamlit: 1.24.1

2023-07-19 16:01:03.621 `st.cache` is deprecated. Please use one of Streamlit's new caching commands,
`st.cache_data` or `st.cache_resource`.

More information [in our docs](https://docs.streamlit.io/library/advanced-features/caching).
Last updated: 2023-07-19T16:01:03.712794-07:00

Python implementation: CPython
Python version       : 3.11.4
IPython version      : 8.14.0

Compiler    : MSC v.1935 64 bit (AMD64)
OS          : Windows
Release     : 10
Machine     : AMD64
Processor   : Intel64 Family 6 Model 154 Stepping 4, GenuineIntel
CPU cores   : 12
Architecture: 64bit

pandas   : 2.0.3
streamlit: 1.24.1

2023-07-19 16:01:03.733 `st.cache` is deprecated. Please use one of Streamlit's new caching commands,
`st.cache_data` or `st.cache_resource`.

More information [in our docs](https://docs.streamlit.io/library/advanced-features/caching).
Wining Hash 00d82f94b6c916eceed5a922a9235112ce57cf518a90ca1371636e4e66e5e2ba
```