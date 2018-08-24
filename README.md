


# quorum-blockchain-starter
Setting up a basic quorum blockchain using truffle


# Pre-requisites
 You will need the following to run this - nodejs, npm, truffle, virtual box, vagrant


# Getting started
Go to quorum blockchain directory and run 

$> vagrant up // This will initialize the cluster

Connect to the culster using 
$> vagrant ssh
 
Now, you must be inside the vagrant VM, change the directory to quorum-examples/7nodes
 $> cd quorum-examples/7nodes/
 
Lets create 7 Quorum nodes that can be used to simulate a real Quorum deployment. 
 $> ./raft-init.sh
 
Nodes will run on 127.0.0.1:22000 to 127.0.0.1:22006 -- 7 nodes on 7 ports

Start the nodes using
$> ./raft-start.sh
 
Your nodes must be up and running. Now change to truffle-app directory

Compile the contracts using 
$> truffle compile 
 
Now, migrate the contracts
$> truffle migrate
 
Migration should complete without any errors. 
Now, you can interact with the contract from truffle consoele

$> truffle console
$> truffle console --network nodefour // to connect to node four
