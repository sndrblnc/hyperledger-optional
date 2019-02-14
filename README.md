STEPS:
1.	Install Hyperledger Fabric pre-requisites including Unbuntu Virtual Machine where the Hyperledger Fabric needs to run. 
2.	Open the Virtual machine then, download and install Go language from https://golang.org/dl/ link that matches up to your operating system.
3.	Go to the directory where the file located, right click to open the terminal.
4.	Type in "tar -C /usr/local -xzf go1.11.5.linux-amd64.tar.gz"
5.	To add Go environment variable, type in 
•	export PATH=$PATH:/usr/local/go/bin
•	export GOPATH=$HOME/go
•	export PATH=$PATH:$GOPATH/bin
6.	After that, we need to clone the fabric-sample project that IBM provided. Clone it by typing “git clone https://github.com/hyperledger/fabric-samples.git” to your terminal. Open the file using “cd fabric-sample”
7.	Afterwards, download the image and binaries by typing in “curl -sSL http://bit.ly/2ysbOFE | bash -s -- 1.4.0" in the terminal.
8.	Go back to the default path using “cd ..” then clone the repository "git clone https://github.com/khrandm/blockchain-training-labs" then go to the fabric-sample folder usibg “cd fablic-sample”
9.	Copy the chaincode and supply from the last cloned project and paste it inside fabric-sample, then merge the file if it lready exists. Open the supply folder, type “cd supply” in the terminal.
10.	 Download the required library for chaincode. Type the following in the terminal.
•	go get github.com/golang/protobuf/proto
•	go get github.com/hyperledger/fabric/common/attrmgr
•	go get github.com/pkg/errors
•	go get github.com/hyperledger/fabric/core/chaincode/lib/cid
11.	now open file manager go to Home/go/src/github.com
12.	copy three folders: hyperledger, pkg, golang then paste it inside fabric-sample/chaincode
13.	Go to fabric-sample/supply and type the following:
•	Type ./startFabric.sh
•	Type npm install
•	Type node enrollAdmin.sh
•	Type node registerSupplier.sh
•	Type node registerOem.sh
•	Type node registerBank.sh
•	Type node app


14.	To check if its running, open the postman application, change the method from GET to POST then add url “localhost:3000/invoice”
15.	below url you should see Params Authroization Headers Body then click Headers
16.	Add another key below Content-Type
17.	type user
18.	and the value would be "supplier"
19.	next open the body tab
20.	click the x-www-form-url-encoded
21.	You should see a form there then type the following below then hit send. You should see result: Success
KEY                      VALUE

invoicenumber          	 INVOICE001
billedto               		 OEM
invoicedate            	 02/08/19
invoiceamount        	 10000
itemdescription      	 KEYBOARD
goodreceived          	 False
ispaid                  		 False
paidamount             	 0
repaid                  	 False
repaymentamount          0
