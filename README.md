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

1. Navigate to my repo: "https://github.com/cannabbeers/18_bank_blockchain" 

2. In the terminal, type: `streamlit run pychain.py`.

3. Enter values for the sender, receiver, and amount, and then click the "Add
Block" button.

        + Do this several times to store several blocks in the ledger.

        + [try the Random Name Generator](https://www.randomlists.com/random-names) for endless supply of senders and receivers to build the *PyChain*

5. Verify the block contents and hashes in the Streamlit drop-down menu.
   ![Block Contents & Hashes](/Images/validate_chain_1.png)
   ![screenshot of the Streamlit application page](/Images/st.cache_data_or_st.cache_resource.png)
   ![screenshot of the Gitbash "Winning Hash"](/Images/gitbash_win_hash.png)
   
7. Test the blockchain validation process by using the web interface.
   ![screenshot of the Streamlit application page validation](/Images/validate_chain_true.png)
   ![screenshot of the GitBash validation](/Images/gitbash_valid.png)




### GITBASH TERMINAL OUTPUT 
