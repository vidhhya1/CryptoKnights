<h1>Bitcoin Scripting Assignment</h1>

    <h2>CS 216: Introduction to Blockchain</h2>

    <h3>Assignment 3: Bitcoin Scripting</h3>

    <h2>Team Members:</h2>
    <ul>
        <li><strong>Name 1</strong> (Roll Number 1)</li>
        <li><strong>Name 2</strong> (Roll Number 2)</li>
        <li><strong>Name 3</strong> (Roll Number 3)</li>
    </ul>

    <h2>Project Overview</h2>
    <p>This project demonstrates the creation and validation of Bitcoin transactions using:</p>
    <ul>
        <li><strong>Legacy (P2PKH) Transactions</strong></li>
        <li><strong>SegWit (P2SH-P2WPKH) Transactions</strong></li>
    </ul>

    <p>We use <strong>Bitcoin Core (bitcoind)</strong> in regtest mode and Python scripts to interact with it via RPC calls. The project includes:</p>
    <ul>
        <li>Setting up a Bitcoin regtest network.</li>
        <li>Creating wallets and generating addresses.</li>
        <li>Funding transactions and analyzing scripts.</li>
        <li>Comparing transaction sizes between Legacy and SegWit formats.</li>
    </ul>

    <hr>

    <h2>Prerequisites</h2>

    <h3>Install Dependencies</h3>
    <p>Ensure you have the following installed:</p>
    <ul>
        <li><strong>Bitcoin Core</strong>: <a href="https://bitcoincore.org/en/download/">Download Bitcoin Core</a></li>
        <li><strong>Python3</strong> (if not installed, install via <code>sudo apt install python3</code> or <code>brew install python3</code>)</li>
        <li><strong>Required Python Libraries</strong>:</li>
    </ul>

    <pre><code>pip install python-bitcoinrpc</code></pre>

    <h3>Configure Bitcoin Core</h3>
    <p>Locate the <code>bitcoin.conf</code> file (usually in <code>~/.bitcoin/bitcoin.conf</code> on Linux/macOS or <code>C:\Users\YourUser\AppData\Roaming\Bitcoin\bitcoin.conf</code> on Windows).</p>
    
    <p>Add the following configuration for regtest mode:</p>
    <pre><code>
regtest=1
server=1
rpcuser=your_rpc_user
rpcpassword=your_rpc_password
rpcport=18443
txindex=1
    </code></pre>

    <p>Start bitcoind in regtest mode:</p>
    <pre><code>bitcoind -regtest -daemon</code></pre>

    <hr>

    <h2>Running the Project</h2>

    <h3>Step 1: Start Bitcoin Daemon</h3>
    <pre><code>bitcoind -regtest -daemon</code></pre>

    <h3>Step 2: Run the Legacy Transaction Script</h3>
    <pre><code>python legacy_transactions.py</code></pre>

    <p>This will:</p>
    <ul>
        <li>Create a wallet</li>
        <li>Generate addresses A, B, C</li>
        <li>Fund address A</li>
        <li>Create a transaction from A → B</li>
        <li>Create a transaction from B → C</li>
        <li>Decode and analyze transactions</li>
    </ul>

    <h3>Step 3: Run the SegWit Transaction Script</h3>
    <pre><code>python segwit_transactions.py</code></pre>

    <p>This follows the same process as above but using P2SH-SegWit addresses.</p>

    <h3>Step 4: Analyze Transactions</h3>
    <ul>
        <li>Check decoded transactions in the output.</li>
        <li>Use Bitcoin Debugger to verify script execution.</li>
    </ul>

    <hr>

    <h2>Expected Output</h2>

    <p>Upon running the scripts, you should see:</p>
    <ul>
        <li><strong>Wallet and Address Creation</strong></li>
        <li><strong>Transaction IDs for A → B and B → C</strong></li>
        <li><strong>Decoded Scripts (locking & unlocking mechanisms)</strong></li>
        <li><strong>Transaction size comparison between Legacy and SegWit</strong></li>
    </ul>

    <hr>

    
