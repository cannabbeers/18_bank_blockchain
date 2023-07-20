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

4. Verify the block contents and hashes in the Streamlit drop-down menu.  Test the blockchain validation process by using the web interface.
   ![Full Ledger](/Images/full_ledger.gif)
   ![screenshot of the Streamlit application page -'Genesis Block'](/Images/genesis_block.gif)

5. Test the blockchain validation process by using the web interface
   ![screenshot of the Gitbash "Winning Hash" & "Blockchain is Valid"](/Images/gitbash_valid_and_win_hash.gif)
   ![screenshot of the Streamlit application page validation](/Images/validate_true.gif)

### GITBASH TERMINAL OUTPUT 

        Blockchain is Valid
        Last updated: 2023-07-19T18:50:02.176629-07:00
        
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

        
## Contributors

Mark Beers: 
[Linked In](https://www.linkedin.com/in/markwbeers/)
---

## License

MIT 

