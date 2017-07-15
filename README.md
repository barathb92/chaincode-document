<span style="font-variant: normal"><font color="#404040"><font face="Roboto Slab, ff-tisa-web-pro, Georgia, Arial, sans-serif"><font size="5" style="font-size: 19pt"><span style="letter-spacing: normal"><span style="font-style: normal">**Chaincode**</span></span></font></font></font></span>

<span style="font-variant: normal"><font color="#00000a"><font size="3" style="font-size: 12pt"><span style="letter-spacing: normal"><span lang="en-US"><span style="font-style: normal"><span style="font-weight: normal">Chaincode is a piece of code that is written in one of the supported languages such "GO" or "Java" and deployed through SDK or CLI into a network of</span></span></span></span></font></font></span> <font color="#000080"><span lang="zxx">[<span style="font-variant: normal"><font color="#9b59b6"><span style="text-decoration: none"><font face="Lato, proxima-nova, Helvetica Neue, Arial, sans-serif"><font size="3" style="font-size: 12pt"><span style="letter-spacing: normal"><span style="font-style: normal"><span style="font-weight: normal">Hyperledger fabric </span></span></span></font></font></span></font></span>](https://gerrit.hyperledger.org/r/#/admin/projects/fabric)</span></font><span style="font-variant: normal"><font color="#00000a"><span style="text-decoration: none"><font size="3" style="font-size: 12pt"><span style="letter-spacing: normal"><span lang="en-US"><span style="font-style: normal"></span></span></span></font></span></font></span><span style="font-variant: normal"><font color="#00000a"><font size="3" style="font-size: 12pt"><span style="letter-spacing: normal"><span lang="en-US"><span style="font-style: normal"><span style="font-weight: normal">peer nodes that enables interaction with that network's shared ledger.</span></span></span></span></font></font></span>

<span style="font-variant: normal"><font color="#00000a"><font size="3" style="font-size: 12pt"><span style="letter-spacing: normal"><span lang="en-US"><span style="font-style: normal"><span style="font-weight: normal">There are 3 aspects to chaincode development :</span></span></span></span></font></font></span>

*   <span style="font-variant: normal"><font color="#ed6a43"><font face="Consolas, Liberation Mono, Menlo, Courier, monospace"><font size="3" style="font-size: 12pt"><span style="letter-spacing: normal"><span lang="en-US"><span style="font-style: normal"><span style="font-weight: normal"> The interfaces that the chaincode shoud implement</span></span></span></span></font></font></span>

*   <span style="font-variant: normal"><font color="#ed6a43"><font face="Consolas, Liberation Mono, Menlo, Courier, monospace"><font size="3" style="font-size: 12pt"><span style="letter-spacing: normal"><span lang="en-US"><span style="font-style: normal"><span style="font-weight: normal"> APIs chaincode can use to interact with the fabric</span></span></span></span></font></font></span>

*   <span style="font-variant: normal"><font color="#ed6a43"><font face="Consolas, Liberation Mono, Menlo, Courier, monospace"><font size="3" style="font-size: 12pt"><span style="letter-spacing: normal"><span lang="en-US"><span style="font-style: normal"><span style="font-weight: normal"> The response from the chaincode</span></span></span></span></font></font></span>

## <span style="font-variant: normal"><font color="#404040"><font face="Roboto Slab, ff-tisa-web-pro, Georgia, Arial, sans-serif"><font size="5" style="font-size: 19pt"><span style="letter-spacing: normal"><span lang="en-US"><span style="font-style: normal">**Chaincode Interfaces**</span></span></span></font></font></font></span>

<span style="font-variant: normal"><font color="#00000a"><font size="3" style="font-size: 12pt"><span style="letter-spacing: normal"><span lang="en-US"><span style="font-style: normal"><span style="font-weight: normal">A chaincode implement the Chaincode Interface that supports two methods :</span></span></span></span></font></font></span>

*   <span style="font-variant: normal"><font color="#ed6a43"><font face="Consolas, Liberation Mono, Menlo, Courier, monospace"><font size="3" style="font-size: 12pt"><span style="letter-spacing: normal"><span lang="en-US"><span style="font-style: normal"><span style="font-weight: normal">Init</span></span></span></span></font></font></span>

*   <span style="font-variant: normal"><font color="#ed6a43"><font face="Consolas, Liberation Mono, Menlo, Courier, monospace"><font size="3" style="font-size: 12pt"><span style="letter-spacing: normal"><span lang="en-US"><span style="font-style: normal"><span style="font-weight: normal">Invoke</span></span></span></span></font></font></span>

<span style="font-variant: normal"><font color="#404040"><font face="Roboto Slab, ff-tisa-web-pro, Georgia, Arial, sans-serif"><font size="4" style="font-size: 14pt"><span style="letter-spacing: normal"><span style="font-style: normal">**Init()** </span></span></span></span></font></font></span>

<span style="font-variant: normal"><font color="#404040"><font face="Roboto Slab, ff-tisa-web-pro, Georgia, Arial, sans-serif"><font size="4" style="font-size: 14pt"><span style="letter-spacing: normal"><span style="font-style: normal">Init is called when you first deploy your chaincode. As the name implies, this function should be used to do any initialization your chaincode needs.</span></span></span></span></font></font></span>

<span style="font-variant: normal"><font color="#404040"><font face="Roboto Slab, ff-tisa-web-pro, Georgia, Arial, sans-serif"><font size="4" style="font-size: 14pt"><span style="letter-spacing: normal"><span style="font-style: normal">**Invoke()**</span></span></span></span></font></font></span> 

<span style="font-variant: normal"><font color="#404040"><font face="Roboto Slab, ff-tisa-web-pro, Georgia, Arial, sans-serif"><font size="4" style="font-size: 14pt"><span style="letter-spacing: normal"><span style="font-style: normal">Invoke is called when you want to call chaincode functions to do real work. Invocations will be captured as a transactions, which get grouped into blocks on the chain. When you need to update or query the ledger, you will do so by invoking your chaincode.</span></span></span></span></font></font></span>

## <span style="font-variant: normal"><font color="#404040"><font face="Roboto Slab, ff-tisa-web-pro, Georgia, Arial, sans-serif"><font size="5" style="font-size: 19pt"><span style="letter-spacing: normal"><span lang="en-US"><span style="font-style: normal">**Dependencies**</span></span></span></font></font></font></span>

<span style="font-variant: normal"><font color="#00000a"><font size="3" style="font-size: 12pt"><span style="letter-spacing: normal"><span lang="en-US"><span style="font-style: normal"><span style="font-weight: normal">The import statement lists a few dependencies that you will need for your chaincode to build successfully.</span></span></span></span></font></font></span>

*   <span style="font-variant: normal"><font color="#ed6a43"><font face="Consolas, Liberation Mono, Menlo, Courier, monospace"><font size="3" style="font-size: 12pt"><span style="letter-spacing: normal"><span lang="en-US"><span style="font-style: normal"><span style="font-weight: normal">fmt</span></span></span></span></font></font></font></span> <span style="font-variant: normal"><font color="#333333"><font face="Consolas, Liberation Mono, Menlo, Courier, monospace"><font size="2" style="font-size: 10pt"><span style="letter-spacing: normal"><span style="font-style: normal"><span style="font-weight: normal">–</span></span></span></font></font></font></span> <span style="font-variant: normal"><font color="#333333"><font face="apple-system, BlinkMacSystemFont, Segoe UI, Helvetica, Arial, sans-serif, Apple Color Emoji, Segoe UI Emoji, Segoe UI Symbol"><font size="3" style="font-size: 12pt"><span style="letter-spacing: normal"><span style="font-style: normal"><span style="font-weight: normal"></span></span></span></font></font></font></span> <span style="font-variant: normal"><font color="#00000a"><font size="3" style="font-size: 12pt"><span style="letter-spacing: normal"><span lang="en-US"><span style="font-style: normal"><span style="font-weight: normal">contains Println for debugging/logging</span></span></span></span></font></font></span><span style="font-variant: normal"><font color="#333333"><font face="apple-system, BlinkMacSystemFont, Segoe UI, Helvetica, Arial, sans-serif, Apple Color Emoji, Segoe UI Emoji, Segoe UI Symbol"><font size="3" style="font-size: 12pt"><span style="letter-spacing: normal"><span style="font-style: normal"><span style="font-weight: normal">.</span></span></span></font></font></font></span>

*   <span style="font-variant: normal"><font color="#ed6a43"><font face="Consolas, Liberation Mono, Menlo, Courier, monospace"><font size="3" style="font-size: 12pt"><span style="letter-spacing: normal"><span lang="en-US"><span style="font-style: normal"><span style="font-weight: normal">errors</span></span></span></span></font></font></font></span> <span style="font-variant: normal"><font color="#333333"><font face="Consolas, Liberation Mono, Menlo, Courier, monospace"><font size="2" style="font-size: 10pt"><span style="letter-spacing: normal"><span style="font-style: normal"><span style="font-weight: normal">–</span></span></span></font></font></font></span> <span style="font-variant: normal"><font color="#333333"><font face="apple-system, BlinkMacSystemFont, Segoe UI, Helvetica, Arial, sans-serif, Apple Color Emoji, Segoe UI Emoji, Segoe UI Symbol"><font size="3" style="font-size: 12pt"><span style="letter-spacing: normal"><span style="font-style: normal"><span style="font-weight: normal"></span></span></span></font></font></font></span> <span style="font-variant: normal"><font color="#00000a"><font size="3" style="font-size: 12pt"><span style="letter-spacing: normal"><span lang="en-US"><span style="font-style: normal"><span style="font-weight: normal">standard go error format.</span></span></span></span></font></font></span>

*   <font color="#000080"><span lang="zxx"><span style="font-variant: normal"><font color="#9b59b6"><span style="text-decoration: none"><font face="Lato, proxima-nova, Helvetica Neue, Arial, sans-serif"><font size="3" style="font-size: 12pt"><span style="letter-spacing: normal"><span style="font-style: normal"><span style="font-weight: normal">[shim](github.com/hyperledger/fabric/core/chaincode/shim)</span></span></span></span></font></font></font></span> <span style="font-variant: normal"><font color="#333333"><font face="Consolas, Liberation Mono, Menlo, Courier, monospace"><font size="2" style="font-size: 10pt"><span style="letter-spacing: normal"><span style="font-style: normal"><span style="font-weight: normal">–</span></span></span></font></font></font></span> <span style="font-variant: normal"><font color="#333333"><font face="apple-system, BlinkMacSystemFont, Segoe UI, Helvetica, Arial, sans-serif, Apple Color Emoji, Segoe UI Emoji, Segoe UI Symbol"><font size="3" style="font-size: 12pt"><span style="letter-spacing: normal"><span style="font-style: normal"><span style="font-weight: normal"></span></span></span></font></font></font></span> <span style="font-variant: normal"><font color="#00000a"><font size="3" style="font-size: 12pt"><span style="letter-spacing: normal"><span lang="en-US"><span style="font-style: normal"><span style="font-weight: normal">contains the definition for the chaincode interface and the chaincode stub, which you will need to interact with the ledger.</span></span></span></span></font></font></span>

##<span style="font-variant: normal"><font color="#404040"><font face="Roboto Slab, ff-tisa-web-pro, Georgia, Arial, sans-serif"><font size="5" style="font-size: 19pt"><span style="letter-spacing: normal"><span style="font-style: normal">**Chaincode APIs**</span></span></font></font></font></span>

<font size="3" style="font-size: 12pt">When the</font> <span style="font-variant: normal"><font color="#ed6a43"><font face="Consolas, Liberation Mono, Menlo, Courier, monospace"><font size="3" style="font-size: 12pt"><span style="letter-spacing: normal"><span style="font-style: normal"><span style="font-weight: normal">Init</span></span></span></font></font></font></span> <font size="3" style="font-size: 12pt">or</font> <span style="font-variant: normal"><font color="#ed6a43"><font face="Consolas, Liberation Mono, Menlo, Courier, monospace"><font size="3" style="font-size: 12pt"><span style="letter-spacing: normal"><span style="font-style: normal"><span style="font-weight: normal">Invoke</span></span></span></font></font></font></span> <font size="3" style="font-size: 12pt">function of a chaincode is called, the fabric passes the</font> <span style="font-variant: normal"><font color="#ed6a43"><font face="Consolas, Liberation Mono, Menlo, Courier, monospace"><font size="3" style="font-size: 12pt"><span style="letter-spacing: normal"><span style="font-style: normal"><span style="font-weight: normal">stub</span></span></span></font></font></font></span> <span style="font-variant: normal"><font color="#333333"><font size="3" style="font-size: 12pt"><span style="letter-spacing: normal"></span></font></font></span> <span style="font-variant: normal"><font color="#ed6a43"><font face="Consolas, Liberation Mono, Menlo, Courier, monospace"><font size="3" style="font-size: 12pt"><span style="letter-spacing: normal"><span style="font-style: normal"><span style="font-weight: normal">shim</span></span></span></font></font></font></span><span style="font-variant: normal"><font color="#333333"><font face="Consolas, Liberation Mono, Menlo, Courier, monospace"><font size="3" style="font-size: 12pt"><span style="letter-spacing: normal"><span style="font-style: normal"><span style="font-weight: normal">.</span></span></span></font></font></font></span><span style="font-variant: normal"><font color="#ed6a43"><font face="Consolas, Liberation Mono, Menlo, Courier, monospace"><font size="3" style="font-size: 12pt"><span style="letter-spacing: normal"><span style="font-style: normal"><span style="font-weight: normal">ChaincodeStubInterface</span></span></span></font></font></font></span> <font size="3" style="font-size: 12pt">parameter and the chaincode returns a</font> <span style="font-variant: normal"><font color="#ed6a43"><font face="Consolas, Liberation Mono, Menlo, Courier, monospace"><font size="3" style="font-size: 12pt"><span style="letter-spacing: normal"><span style="font-style: normal"><span style="font-weight: normal">pb</span></span></span></font></font></font></span><span style="font-variant: normal"><font color="#333333"><font face="Consolas, Liberation Mono, Menlo, Courier, monospace"><font size="3" style="font-size: 12pt"><span style="letter-spacing: normal"><span style="font-style: normal"><span style="font-weight: normal">.</span></span></span></font></font></font></span><span style="font-variant: normal"><font color="#ed6a43"><font face="Consolas, Liberation Mono, Menlo, Courier, monospace"><font size="3" style="font-size: 12pt"><span style="letter-spacing: normal"><span style="font-style: normal"><span style="font-weight: normal">Response</span></span></span></font></font></font></span><font size="3" style="font-size: 12pt">. This stub can be used to call APIs to access to the ledger services, transaction context, or to invoke other chaincodes.</font>

<font size="3" style="font-size: 12pt">The current APIs are defined in the shim package, generated by</font> <span style="font-variant: normal"><font color="#ed6a43"><font face="Consolas, Liberation Mono, Menlo, Courier, monospace"><font size="3" style="font-size: 12pt"><span style="letter-spacing: normal"><span style="font-style: normal"><span style="font-weight: normal">godoc github.com/hyperledger/fabric/core/chaincode/shim</span></span></span></font></font></font></span> <span style="font-variant: normal"><font color="#00000a"><font size="3" style="font-size: 12pt"><span style="letter-spacing: normal"><span lang="en-US"><span style="font-style: normal"><span style="font-weight: normal">command</span></span></span></span></font></font></span><font size="3" style="font-size: 12pt">. You can refer to</font> <font color="#000080"><span lang="zxx">[<span style="font-variant: normal"><font color="#9b59b6"><span style="text-decoration: none"><font face="Lato, proxima-nova, Helvetica Neue, Arial, sans-serif"><font size="3" style="font-size: 12pt"><span style="letter-spacing: normal"><span lang="zxx"><span style="font-style: normal"><span style="font-weight: normal">shim here</span></span></span></span></font></font></span></font></span>](https://github.com/hyperledger/fabric/blob/master/core/chaincode/shim)</span></font><font size="3" style="font-size: 12pt">. However, it also includes functions from</font> <font color="#000080"><span lang="zxx">[<span style="font-variant: normal"><font color="#9b59b6"><span style="text-decoration: none"><font face="Lato, proxima-nova, Helvetica Neue, Arial, sans-serif"><font size="3" style="font-size: 12pt"><span style="letter-spacing: normal"><span lang="zxx"><span style="font-style: normal"><span style="font-weight: normal">chaincode.pb.go</span></span></span></span></font></font></span></font></span>](https://github.com/hyperledger/fabric/blob/master/protos/peer/chaincode.pb.go)</span></font> <font size="3" style="font-size: 12pt">with an “_” included in its name such as func (*Column) XXX_OneofFuncs that are not intended as public API. The best is to look at the function definitions in</font> <font color="#000080"><span lang="zxx">[<span style="font-variant: normal"><font color="#9b59b6"><span style="text-decoration: none"><font face="Lato, proxima-nova, Helvetica Neue, Arial, sans-serif"><font size="3" style="font-size: 12pt"><span style="letter-spacing: normal"><span lang="zxx"><span style="font-style: normal"><span style="font-weight: normal">chaincode.go</span></span></span></span></font></font></span></font></span>](https://github.com/hyperledger/fabric/blob/master/core/chaincode/shim/chaincode.go)</span></font> <font size="3" style="font-size: 12pt">and</font> <font color="#000080"><span lang="zxx">[<span style="font-variant: normal"><font color="#9b59b6"><span style="text-decoration: none"><font face="Lato, proxima-nova, Helvetica Neue, Arial, sans-serif"><font size="3" style="font-size: 12pt"><span style="letter-spacing: normal"><span lang="zxx"><span style="font-style: normal"><span style="font-weight: normal">chaincode example</span></span></span></span></font></font></span></font></span>](https://github.com/hyperledger/fabric/tree/master/examples/chaincode/chaintool/example02/src/chaincode)</span></font> <font size="3" style="font-size: 12pt">for usage.</font>

##<span style="font-variant: normal"><font color="#404040"><font face="Roboto Slab, ff-tisa-web-pro, Georgia, Arial, sans-serif"><font size="5" style="font-size: 19pt"><span style="letter-spacing: normal"><span lang="en-US"><span style="font-style: normal">**Response**</span></span></span></font></font></font></span>

<span style="font-variant: normal"><font color="#00000a"><font size="3" style="font-size: 12pt"><span style="letter-spacing: normal"><span lang="en-US"><span style="font-style: normal"><span style="font-weight: normal">The response from the chaincode is in the form of protobuffer.</span></span></span></span></font></font></span> <span style="font-variant: normal"><font color="#404040"><font face="Roboto Slab, ff-tisa-web-pro, Georgia, Arial, sans-serif"><font size="3" style="font-size: 12pt"><span style="letter-spacing: normal"><span lang="en-US"><span style="font-style: normal"></span></span></span></font></font></font></span><span style="font-variant: normal"><font color="#a71d5d"><font face="Consolas, Liberation Mono, Menlo, Courier, monospace"><font size="2" style="font-size: 9pt"><span style="letter-spacing: normal"><span lang="en-US"><span style="font-style: normal">
```
message Response {	
	
	// A status code that should follow the HTTP status codes. 
	int32 status = 1; 

	// A message associated with the response code. 
	string message = 2; 

	// A payload that can be used to include metadata with this response. 
	bytes payload = 3;

}
```
The chaincode also returns events :

```
messageEvent {  

    oneof Event {

    //Register consumer sent event  
    Register register = 1;

    //producer events common.  
    Block block = 2;  
    ChaincodeEvent chaincodeEvent = 3;  
    Rejection rejection = 4;

    //Unregister consumer sent events  
    Unregister unregister = 5;  

    }  

}
```

```
messageChaincodeEvent {

    string chaincodeID = 1;  
    string txID = 2;  
    string eventName = 3;  
    bytes payload = 4;

}
```


<span style="font-variant: normal"><font color="#00000a"><font face="Liberation Serif, serif"><font size="3" style="font-size: 12pt"><span style="letter-spacing: normal"><span lang="en-US"><span style="font-style: normal"><span style="font-weight: normal">Once developed and deployed, there are two ways to interact with the chaincode - through SDK or CLI. The steps for CLI are as described below. For SDK interaction, refer the</span></span></span></span></font></font></font></span> <font color="#000080"><span lang="zxx"><u>[<span style="font-variant: normal"><font color="#00000a"><font face="Liberation Serif, serif"><font size="3" style="font-size: 12pt"><span style="letter-spacing: normal"><span lang="en-US"><span style="font-style: normal"><span style="font-weight: normal">examples here</span></span></span></span></font></font></font></span>](https://github.com/hyperledger/fabric-sdk-node/tree/master/examples/balance-transfer)</u></span></font><span style="font-variant: normal"><font color="#00000a"><font face="Liberation Serif, serif"><font size="3" style="font-size: 12pt"><span style="letter-spacing: normal"><span lang="en-US"><span style="font-style: normal"><span style="font-weight: normal">.</span></span></span></span></font></font></font></span>


##  <span style="font-variant: normal"><font color="#404040"><font face="Roboto Slab, ff-tisa-web-pro, Georgia, Arial, sans-serif"><font size="5" style="font-size: 19pt"><span style="letter-spacing: normal"><span style="font-style: normal">**Command-line Interface (CLI)**</span></span></font></font></font></span>

<span style="font-variant: normal"><font color="#404040"><font face="Lato, proxima-nova, Helvetica Neue, Arial, sans-serif"><font size="3" style="font-size: 12pt"><span style="letter-spacing: normal"><span style="font-style: normal"><span style="font-weight: normal">To view the currently available CLI commands, execute the following:</span></span></span></font></font></font></span>
```
    cd /opt/gopath/src/github.com/hyperledger/fabric
    build /bin/peer
```

<span style="font-variant: normal"><font color="#404040"><font face="Lato, proxima-nova, Helvetica Neue, Arial, sans-serif"><font size="3" style="font-size: 12pt"><span style="letter-spacing: normal"><span style="font-style: normal"><span style="font-weight: normal">You will see output similar to the example below (</span></span></span></font></font></font></span>**<span style="font-variant: normal"><font color="#404040"><font face="Lato, proxima-nova, Helvetica Neue, Arial, sans-serif"><font size="3" style="font-size: 12pt"><span style="letter-spacing: normal"><span style="font-style: normal">**NOTE:**</span></span></font></font></font></span>**<span style="font-variant: normal"><font color="#404040"><font face="Lato, proxima-nova, Helvetica Neue, Arial, sans-serif"><font size="3" style="font-size: 12pt"><span style="letter-spacing: normal"><span style="font-style: normal"><span style="font-weight: normal"> rootcommand below is hardcoded in </span></span></span></font></font></font></span><font color="#000080"><span lang="zxx">[<span style="font-variant: normal"><font color="#9b59b6"><span style="text-decoration: none"><font face="Lato, proxima-nova, Helvetica Neue, Arial, sans-serif"><font size="3" style="font-size: 12pt"><span style="letter-spacing: normal"><span style="font-style: normal"><span style="font-weight: normal">main.go</span></span></span></font></font></span></font></span>](https://github.com/hyperledger/fabric/blob/master/main.go)</span></font><span style="font-variant: normal"><font color="#404040"><font face="Lato, proxima-nova, Helvetica Neue, Arial, sans-serif"><font size="3" style="font-size: 12pt"><span style="letter-spacing: normal"><span style="font-style: normal"><span style="font-weight: normal">. Currently, the build will create a </span></span></span></font></font></font></span>_<span style="font-variant: normal"><font color="#404040"><font face="Lato, proxima-nova, Helvetica Neue, Arial, sans-serif"><font size="3" style="font-size: 12pt"><span style="letter-spacing: normal"><span style="font-style: normal"><span style="font-weight: normal">peer</span></span></span></font></font></font></span>_<span style="font-variant: normal"><font color="#404040"><font face="Lato, proxima-nova, Helvetica Neue, Arial, sans-serif"><font size="3" style="font-size: 12pt"><span style="letter-spacing: normal"><span style="font-style: normal"><span style="font-weight: normal"> executable file).</span></span></span></font></font></font></span>

```
    Usage:
      peer [flags]
      peer [command]

    Available Commands:
      version     Print fabric peer version.
      node        node specific commands.
      channel     channel specific commands.
      chaincode   chaincode specific commands.
      logging         logging specific commands


    Flags:
      --logging-level string: Default logging level and overrides, see core.yaml for full syntax
      --test.coverprofile string: Done (default “coverage.cov)
      -v, --version: Display current version of fabric peer server
    Use "peer [command] --help" for more information about a command.
```

<span style="font-variant: normal"><font color="#404040"><font face="Lato, proxima-nova, Helvetica Neue, Arial, sans-serif"><font size="3" style="font-size: 12pt"><span style="letter-spacing: normal"><span style="font-style: normal"><span style="font-weight: normal">The </span></span></span></font></font></font></span><span style="display: inline-block; border: 1px solid #e1e4e5; padding: 0.01in"><span style="font-variant: normal"><font color="#e74c3c"><font face="Consolas, Andale Mono WT, Andale Mono, Lucida Console, Lucida Sans Typewriter, DejaVu Sans Mono, Bitstream Vera Sans Mono, Liberation Mono, Nimbus Mono L, Monaco, Courier New, Courier, monospace"><font size="2" style="font-size: 9pt"><span style="letter-spacing: normal"><span style="font-style: normal"><span style="font-weight: normal">`peer`</span></span></span></font></font></font></span></span><span style="font-variant: normal"><font color="#404040"><font face="Lato, proxima-nova, Helvetica Neue, Arial, sans-serif"><font size="3" style="font-size: 12pt"><span style="letter-spacing: normal"><span style="font-style: normal"><span style="font-weight: normal"> command supports several subcommands and flags, as shown above. To facilitate its use in scripted applications, the </span></span></span></font></font></font></span><span style="display: inline-block; border: 1px solid #e1e4e5; padding: 0.01in"><span style="font-variant: normal"><font color="#e74c3c"><font face="Consolas, Andale Mono WT, Andale Mono, Lucida Console, Lucida Sans Typewriter, DejaVu Sans Mono, Bitstream Vera Sans Mono, Liberation Mono, Nimbus Mono L, Monaco, Courier New, Courier, monospace"><font size="2" style="font-size: 9pt"><span style="letter-spacing: normal"><span style="font-style: normal"><span style="font-weight: normal">`peer`</span></span></span></font></font></font></span></span><span style="font-variant: normal"><font color="#404040"><font face="Lato, proxima-nova, Helvetica Neue, Arial, sans-serif"><font size="3" style="font-size: 12pt"><span style="letter-spacing: normal"><span style="font-style: normal"><span style="font-weight: normal"> command always produces a non-zero return code in the event of command failure. Upon success, many of the subcommands produce a result on </span></span></span></font></font></font></span>**<span style="font-variant: normal"><font color="#404040"><font face="Lato, proxima-nova, Helvetica Neue, Arial, sans-serif"><font size="3" style="font-size: 12pt"><span style="letter-spacing: normal"><span style="font-style: normal">**stdout**</span></span></font></font></font></span>**<span style="font-variant: normal"><font color="#404040"><font face="Lato, proxima-nova, Helvetica Neue, Arial, sans-serif"><font size="3" style="font-size: 12pt"><span style="letter-spacing: normal"><span style="font-style: normal"><span style="font-weight: normal"> as shown in the table below:</span></span></span></font></font></font></span>

<table width="665" cellpadding="8" cellspacing="0"><colgroup><col width="262"> <col width="371"></colgroup>

<thead>

<tr>

<th width="262" bgcolor="#ffffff" style="border-top: none; border-bottom: 1.50pt solid #e1e4e5; border-left: none; border-right: none; padding-top: 0in; padding-bottom: 0.08in; padding-left: 0in; padding-right: 0in">

<font size="2" style="font-size: 9pt">Command</font>

</th>

<th width="371" bgcolor="#ffffff" style="border-top: none; border-bottom: 1.50pt solid #e1e4e5; border-left: none; border-right: none; padding-top: 0in; padding-bottom: 0.08in; padding-left: 0in; padding-right: 0in">

<font size="2" style="font-size: 9pt">stdout</font><font size="2" style="font-size: 9pt"> result in the event of success</font>

</th>

</tr>

</thead>

<tbody>

<tr>

<td width="262" bgcolor="#f3f6f6" style="border-top: 1px solid #e1e4e5; border-bottom: 1px solid #e1e4e5; border-left: 1px solid #e1e4e5; border-right: none; padding-top: 0in; padding-bottom: 0.08in; padding-left: 0.16in; padding-right: 0in">

<span style="display: inline-block; border: 1px solid #e1e4e5; padding: 0.01in"><font color="#e74c3c"><font face="Consolas, Andale Mono WT, Andale Mono, Lucida Console, Lucida Sans Typewriter, DejaVu Sans Mono, Bitstream Vera Sans Mono, Liberation Mono, Nimbus Mono L, Monaco, Courier New, Courier, monospace"><font size="1" style="font-size: 7pt">version</font></font></font></span>

</td>

<td width="371" bgcolor="#f3f6f6" style="border-top: 1px solid #e1e4e5; border-bottom: 1px solid #e1e4e5; border-left: 1px solid #e1e4e5; border-right: none; padding-top: 0in; padding-bottom: 0.08in; padding-left: 0.16in; padding-right: 0in">

<font size="2" style="font-size: 9pt">String form of </font><span style="display: inline-block; border: 1px solid #e1e4e5; padding: 0.01in"><font color="#e74c3c"><font face="Consolas, Andale Mono WT, Andale Mono, Lucida Console, Lucida Sans Typewriter, DejaVu Sans Mono, Bitstream Vera Sans Mono, Liberation Mono, Nimbus Mono L, Monaco, Courier New, Courier, monospace"><font size="1" style="font-size: 7pt">peer.version</font></font></font></span><font size="2" style="font-size: 9pt"> defined in </font><font color="#000080"><span lang="zxx">core.yaml (https://github.com/hyperledger/fabric/blob/master/peer/core.yaml)</span></font>

</td>

</tr>

<tr>

<td width="262" bgcolor="#ffffff" style="border-top: 1px solid #e1e4e5; border-bottom: 1px solid #e1e4e5; border-left: 1px solid #e1e4e5; border-right: none; padding-top: 0in; padding-bottom: 0.08in; padding-left: 0.16in; padding-right: 0in">

<span style="display: inline-block; border: 1px solid #e1e4e5; padding: 0.01in"><font color="#e74c3c"><font face="Consolas, Andale Mono WT, Andale Mono, Lucida Console, Lucida Sans Typewriter, DejaVu Sans Mono, Bitstream Vera Sans Mono, Liberation Mono, Nimbus Mono L, Monaco, Courier New, Courier, monospace"><font size="1" style="font-size: 7pt">node start</font></font></font></span>

</td>

<td width="371" bgcolor="#ffffff" style="border-top: 1px solid #e1e4e5; border-bottom: 1px solid #e1e4e5; border-left: 1px solid #e1e4e5; border-right: none; padding-top: 0in; padding-bottom: 0.08in; padding-left: 0.16in; padding-right: 0in">

<font size="2" style="font-size: 9pt">N/A</font>

</td>

</tr>

<tr>

<td width="262" bgcolor="#f3f6f6" style="border-top: 1px solid #e1e4e5; border-bottom: 1px solid #e1e4e5; border-left: 1px solid #e1e4e5; border-right: none; padding-top: 0in; padding-bottom: 0.08in; padding-left: 0.16in; padding-right: 0in">

<span style="display: inline-block; border: 1px solid #e1e4e5; padding: 0.01in"><font color="#e74c3c"><font face="Consolas, Andale Mono WT, Andale Mono, Lucida Console, Lucida Sans Typewriter, DejaVu Sans Mono, Bitstream Vera Sans Mono, Liberation Mono, Nimbus Mono L, Monaco, Courier New, Courier, monospace"><font size="1" style="font-size: 7pt">node status</font></font></font></span>

</td>

<td width="371" bgcolor="#f3f6f6" style="border-top: 1px solid #e1e4e5; border-bottom: 1px solid #e1e4e5; border-left: 1px solid #e1e4e5; border-right: none; padding-top: 0in; padding-bottom: 0.08in; padding-left: 0.16in; padding-right: 0in">

<font size="2" style="font-size: 9pt">String form of StatusCode (https://github.com/hyperledger/fabric/blob/master/protos/server_admin.proto#L36)</font>

</td>

</tr>

<tr>

<td width="262" bgcolor="#ffffff" style="border-top: 1px solid #e1e4e5; border-bottom: 1px solid #e1e4e5; border-left: 1px solid #e1e4e5; border-right: none; padding-top: 0in; padding-bottom: 0.08in; padding-left: 0.16in; padding-right: 0in">

<span style="display: inline-block; border: 1px solid #e1e4e5; padding: 0.01in"><font color="#e74c3c"><font face="Consolas, Andale Mono WT, Andale Mono, Lucida Console, Lucida Sans Typewriter, DejaVu Sans Mono, Bitstream Vera Sans Mono, Liberation Mono, Nimbus Mono L, Monaco, Courier New, Courier, monospace"><font size="1" style="font-size: 7pt">node stop</font></font></font></span>

</td>

<td width="371" bgcolor="#ffffff" style="border-top: 1px solid #e1e4e5; border-bottom: 1px solid #e1e4e5; border-left: 1px solid #e1e4e5; border-right: none; padding-top: 0in; padding-bottom: 0.08in; padding-left: 0.16in; padding-right: 0in">

<font size="2" style="font-size: 9pt">String form of StatusCode (https://github.com/hyperledger/fabric/blob/master/protos/server_admin.proto#L36)</font>

</td>

</tr>

<tr>

<td width="262" bgcolor="#f3f6f6" style="border-top: 1px solid #e1e4e5; border-bottom: 1px solid #e1e4e5; border-left: 1px solid #e1e4e5; border-right: none; padding-top: 0in; padding-bottom: 0.08in; padding-left: 0.16in; padding-right: 0in">

<span style="display: inline-block; border: 1px solid #e1e4e5; padding: 0.01in"><font color="#e74c3c"><font face="Consolas, Andale Mono WT, Andale Mono, Lucida Console, Lucida Sans Typewriter, DejaVu Sans Mono, Bitstream Vera Sans Mono, Liberation Mono, Nimbus Mono L, Monaco, Courier New, Courier, monospace"><font size="1" style="font-size: 7pt">chaincode deploy</font></font></font></span>

</td>

<td width="371" bgcolor="#f3f6f6" style="border-top: 1px solid #e1e4e5; border-bottom: 1px solid #e1e4e5; border-left: 1px solid #e1e4e5; border-right: none; padding-top: 0in; padding-bottom: 0.08in; padding-left: 0.16in; padding-right: 0in">

<font size="2" style="font-size: 9pt">The chaincode container name (hash) required for subsequent</font><span style="display: inline-block; border: 1px solid #e1e4e5; padding: 0.01in"><font color="#e74c3c"><font face="Consolas, Andale Mono WT, Andale Mono, Lucida Console, Lucida Sans Typewriter, DejaVu Sans Mono, Bitstream Vera Sans Mono, Liberation Mono, Nimbus Mono L, Monaco, Courier New, Courier, monospace"><font size="1" style="font-size: 7pt"> chaincode invoke</font></font></font></span><font size="2" style="font-size: 9pt"> and </font><span style="display: inline-block; border: 1px solid #e1e4e5; padding: 0.01in"><font color="#e74c3c"><font face="Consolas, Andale Mono WT, Andale Mono, Lucida Console, Lucida Sans Typewriter, DejaVu Sans Mono, Bitstream Vera Sans Mono, Liberation Mono, Nimbus Mono L, Monaco, Courier New, Courier, monospace"><font size="1" style="font-size: 7pt">chaincode query</font></font></font></span><font size="2" style="font-size: 9pt"> commands</font>

</td>

</tr>

<tr>

<td width="262" bgcolor="#ffffff" style="border-top: 1px solid #e1e4e5; border-bottom: 1px solid #e1e4e5; border-left: 1px solid #e1e4e5; border-right: none; padding-top: 0in; padding-bottom: 0.08in; padding-left: 0.16in; padding-right: 0in">

<span style="display: inline-block; border: 1px solid #e1e4e5; padding: 0.01in"><font color="#e74c3c"><font face="Consolas, Andale Mono WT, Andale Mono, Lucida Console, Lucida Sans Typewriter, DejaVu Sans Mono, Bitstream Vera Sans Mono, Liberation Mono, Nimbus Mono L, Monaco, Courier New, Courier, monospace"><font size="1" style="font-size: 7pt">chaincode invoke</font></font></font></span>

</td>

<td width="371" bgcolor="#ffffff" style="border-top: 1px solid #e1e4e5; border-bottom: 1px solid #e1e4e5; border-left: 1px solid #e1e4e5; border-right: none; padding-top: 0in; padding-bottom: 0.08in; padding-left: 0.16in; padding-right: 0in">

<font size="2" style="font-size: 9pt">The transaction ID (UUID)</font>

</td>

</tr>

<tr>

<td width="262" bgcolor="#f3f6f6" style="border-top: 1px solid #e1e4e5; border-bottom: 1px solid #e1e4e5; border-left: 1px solid #e1e4e5; border-right: none; padding-top: 0in; padding-bottom: 0.08in; padding-left: 0.16in; padding-right: 0in">

<span style="display: inline-block; border: 1px solid #e1e4e5; padding: 0.01in"><font color="#e74c3c"><font face="Consolas, Andale Mono WT, Andale Mono, Lucida Console, Lucida Sans Typewriter, DejaVu Sans Mono, Bitstream Vera Sans Mono, Liberation Mono, Nimbus Mono L, Monaco, Courier New, Courier, monospace"><font size="1" style="font-size: 7pt">chaincode query</font></font></font></span>

</td>

<td width="371" bgcolor="#f3f6f6" style="border-top: 1px solid #e1e4e5; border-bottom: 1px solid #e1e4e5; border-left: 1px solid #e1e4e5; border-right: none; padding-top: 0in; padding-bottom: 0.08in; padding-left: 0.16in; padding-right: 0in">

<font size="2" style="font-size: 9pt">By default, the query result is formatted as a printable</font>

</td>

</tr>

<tr>

<td width="262" bgcolor="#f3f6f6" style="border-top: 1px solid #e1e4e5; border-bottom: 1px solid #e1e4e5; border-left: 1px solid #e1e4e5; border-right: none; padding-top: 0in; padding-bottom: 0.08in; padding-left: 0.16in; padding-right: 0in">

<span style="display: inline-block; border: 1px solid #e1e4e5; padding: 0.01in"><font color="#e74c3c"><font face="Consolas, Andale Mono WT, Andale Mono, Lucida Console, Lucida Sans Typewriter, DejaVu Sans Mono, Bitstream Vera Sans Mono, Liberation Mono, Nimbus Mono L, Monaco, Courier New, Courier, monospace"><font size="1" style="font-size: 7pt"><span lang="en-US">channel create</span></font></font></font></span>

</td>

<td width="371" bgcolor="#f3f6f6" style="border-top: 1px solid #e1e4e5; border-bottom: 1px solid #e1e4e5; border-left: 1px solid #e1e4e5; border-right: none; padding-top: 0in; padding-bottom: 0.08in; padding-left: 0.16in; padding-right: 0in">

<font color="#00000a"><font size="2" style="font-size: 9pt"><span lang="en-US">Create a chain</span></font></font>

</td>

</tr>

<tr>

<td width="262" bgcolor="#f3f6f6" style="border-top: 1px solid #e1e4e5; border-bottom: 1px solid #e1e4e5; border-left: 1px solid #e1e4e5; border-right: none; padding-top: 0in; padding-bottom: 0.08in; padding-left: 0.16in; padding-right: 0in">

<span style="display: inline-block; border: 1px solid #e1e4e5; padding: 0.01in"><font color="#e74c3c"><font face="Consolas, Andale Mono WT, Andale Mono, Lucida Console, Lucida Sans Typewriter, DejaVu Sans Mono, Bitstream Vera Sans Mono, Liberation Mono, Nimbus Mono L, Monaco, Courier New, Courier, monospace"><font size="1" style="font-size: 7pt"><span lang="en-US">channel join</span></font></font></font></span>

</td>

<td width="371" bgcolor="#f3f6f6" style="border-top: 1px solid #e1e4e5; border-bottom: 1px solid #e1e4e5; border-left: 1px solid #e1e4e5; border-right: none; padding-top: 0in; padding-bottom: 0.08in; padding-left: 0.16in; padding-right: 0in">

<font color="#00000a"><font size="2" style="font-size: 9pt"><span lang="en-US">Adds a peer to the chain</span></font></font>

</td>

</tr>

<tr>

<td width="262" bgcolor="#f3f6f6" style="border-top: 1px solid #e1e4e5; border-bottom: 1px solid #e1e4e5; border-left: 1px solid #e1e4e5; border-right: none; padding-top: 0in; padding-bottom: 0.08in; padding-left: 0.16in; padding-right: 0in">

<pre class="western" style="orphans: 2; widows: 2"><span style="display: inline-block; border: 1px solid #e1e4e5; padding: 0.01in"><span style="font-variant: normal"><font color="#e74c3c"><font face="Consolas, Andale Mono WT, Andale Mono, Lucida Console, Lucida Sans Typewriter, DejaVu Sans Mono, Bitstream Vera Sans Mono, Liberation Mono, Nimbus Mono L, Monaco, Courier New, Courier, monospace"><font size="1" style="font-size: 7pt"><span style="letter-spacing: normal"><span lang="en-US"><span style="font-style: normal"><span style="font-weight: normal">--peer-defaultchain=true</span></span></span></span></font></font></font></span></span></pre>

</td>

<td width="371" bgcolor="#f3f6f6" style="border-top: 1px solid #e1e4e5; border-bottom: 1px solid #e1e4e5; border-left: 1px solid #e1e4e5; border-right: none; padding-top: 0in; padding-bottom: 0.08in; padding-left: 0.16in; padding-right: 0in">

<font color="#00000a"><font size="2" style="font-size: 9pt"><span lang="en-US"> Allows users to continue to work with the default TEST_CHAINID string. Command line options support writing this value as raw bytes (-r, –raw) or formatted as the hexadecimal representation of the raw bytes (-x, –hex). If the query response is empty then nothing is output.</span></font></font>

</td>


</tbody>

</table>

##Deploy a Chaincode

<a name="deploy-a-chaincode"></a><span style="font-variant: normal"><font color="#404040"><font face="Roboto Slab, ff-tisa-web-pro, Georgia, Arial, sans-serif"><font size="4" style="font-size: 16pt"><span style="letter-spacing: normal"><span style="font-style: normal"></span></span></font></font></font></span> <span style="font-variant: normal"><font color="#404040"><font face="Lato, proxima-nova, Helvetica Neue, Arial, sans-serif"><font size="3" style="font-size: 12pt"><span style="letter-spacing: normal"><span style="font-style: normal"><span style="font-weight: normal">Before we deploy the chaincode, we need to create channels and direct the peers to join the channels. Click and follow the instructions to</span></span></span></font></font></font></span> <span style="display: inline-block; border: 1px solid #e1e4e5; padding: 0.01in">[<span style="font-variant: normal"><font color="#dd1144"><font face="Consolas, Andale Mono WT, Andale Mono, Lucida Console, Lucida Sans Typewriter, DejaVu Sans Mono, Bitstream Vera Sans Mono, Liberation Mono, Nimbus Mono L, Monaco, Courier New, Courier, monospace"><font size="1" style="font-size: 7pt"><span style="letter-spacing: normal"><span lang="en-US"><span style="font-style: normal"><span style="font-weight: normal">`create`</span></span></span></span></font></font></font></span>](https://github.com/ratnakar-asara/Fabric_V1.0_Skeletal_Peer/blob/master/mutlichannel.md#create-a-channel)</span> <span style="font-variant: normal"><font color="#404040"><font face="Lato, proxima-nova, Helvetica Neue, Arial, sans-serif"><font size="3" style="font-size: 12pt"><span style="letter-spacing: normal"><span style="font-style: normal"><span style="font-weight: normal">and</span></span></span></font></font></font></span> <span style="display: inline-block; border: 1px solid #e1e4e5; padding: 0.01in">[<span style="font-variant: normal"><font color="#dd1144"><font face="Consolas, Andale Mono WT, Andale Mono, Lucida Console, Lucida Sans Typewriter, DejaVu Sans Mono, Bitstream Vera Sans Mono, Liberation Mono, Nimbus Mono L, Monaco, Courier New, Courier, monospace"><font size="1" style="font-size: 7pt"><span style="letter-spacing: normal"><span lang="en-US"><span style="font-style: normal"><u><span style="font-weight: normal">`join`</span></u></span></span></span></font></font></font></span>](https://github.com/ratnakar-asara/Fabric_V1.0_Skeletal_Peer/blob/master/mutlichannel.md#join-a-channel)</span> <span style="font-variant: normal"><font color="#404040"><font face="Lato, proxima-nova, Helvetica Neue, Arial, sans-serif"><font size="3" style="font-size: 12pt"><span style="letter-spacing: normal"><span style="font-style: normal"><span style="font-weight: normal">a channel.</span></span></span></font></font></font></span>

## Using vagrant, to create and join a channel :

####<span style="font-variant: normal"><font color="#404040"><font face="Lato, proxima-nova, Helvetica Neue, Arial, sans-serif"><font size="3" style="font-size: 12pt"><span style="letter-spacing: normal"><span style="font-style: normal"><span style="font-weight: normal"></span></span></span></font></font></font></span> <span style="font-variant: normal"><font color="#404040"><font face="Lato, proxima-nova, Helvetica Neue, Arial, sans-serif"><font size="3" style="font-size: 12pt"><span style="letter-spacing: normal"><span style="font-style: normal"></span></span></font></font></font></span> <span style="font-variant: normal"><font color="#404040"><font face="Lato, proxima-nova, Helvetica Neue, Arial, sans-serif"><font size="3" style="font-size: 12pt"><span style="letter-spacing: normal"><span style="font-style: normal"><span style="font-weight: normal"></span></span></span></font></font></font></span> <span style="font-variant: normal"><font color="#404040"><font face="Lato, proxima-nova, Helvetica Neue, Arial, sans-serif"><font size="3" style="font-size: 12pt"><span style="letter-spacing: normal"><span lang="en-US"><span style="font-style: normal"><span style="font-weight: normal">Start the orderer</span></span></span></span></font></font></font></span> 

<span style="font-variant: normal"><font color="#404040"><font face="Lato, proxima-nova, Helvetica Neue, Arial, sans-serif"><font size="3" style="font-size: 12pt"><span style="letter-spacing: normal"><span style="font-style: normal"><span style="font-weight: normal"></span></span></span></font></font></font></span> <span style="display: inline-block; border: 1px solid #e1e4e5; padding: 0.01in"><span style="font-variant: normal"><font color="#dd1144"><font face="Consolas, Andale Mono WT, Andale Mono, Lucida Console, Lucida Sans Typewriter, DejaVu Sans Mono, Bitstream Vera Sans Mono, Liberation Mono, Nimbus Mono L, Monaco, Courier New, Courier, monospace"><font size="1" style="font-size: 7pt"><span style="letter-spacing: normal"><span lang="en-US"><span style="font-style: normal"><span style="font-weight: normal">`ORDERER_GENERAL_LOGLEVEL=debug ./orderer`</span></span></span></span></font></font></font></span></span>

####<span style="font-variant: normal"><font color="#404040"><font face="Lato, proxima-nova, Helvetica Neue, Arial, sans-serif"><font size="3" style="font-size: 12pt"><span style="letter-spacing: normal"><span lang="en-US"><span style="font-style: normal"><span style="font-weight: normal">Create a chain</span></span></span></span></font></font></font></span>

<pre class="western"><span style="display: inline-block; border: 1px solid #e1e4e5; padding: 0.01in"><span style="font-variant: normal"><font color="#dd1144"><font face="Consolas, Andale Mono WT, Andale Mono, Lucida Console, Lucida Sans Typewriter, DejaVu Sans Mono, Bitstream Vera Sans Mono, Liberation Mono, Nimbus Mono L, Monaco, Courier New, Courier, monospace"><font size="1" style="font-size: 7pt"><span style="letter-spacing: normal"><span lang="en-US"><span style="font-style: normal"><span style="font-weight: normal">CORE_PEER_MSPCONFIGPATH=/opt/gopath/src/github.com/hyperledger/fabric/msp/sampleconfig peer channel create -c myc1</span></span></span></span></font></font></font></span></span></pre>

####<span style="font-variant: normal"><font color="#404040"><font face="Lato, proxima-nova, Helvetica Neue, Arial, sans-serif"><font size="3" style="font-size: 12pt"><span style="letter-spacing: normal"><span lang="en-US"><span style="font-style: normal"><span style="font-weight: normal">Start peer in chainless mode</span></span></span></span></font></font></font></span>

<pre class="western" style="line-height: 145%; orphans: 2; widows: 2"><span style="display: inline-block; border: 1px solid #e1e4e5; padding: 0.01in"><span style="font-variant: normal"><font color="#dd1144"><font face="Consolas, Andale Mono WT, Andale Mono, Lucida Console, Lucida Sans Typewriter, DejaVu Sans Mono, Bitstream Vera Sans Mono, Liberation Mono, Nimbus Mono L, Monaco, Courier New, Courier, monospace"><font size="1" style="font-size: 7pt"><span style="letter-spacing: normal"><span lang="en-US"><span style="font-style: normal"><span style="font-weight: normal">peer node start --peer-defaultchain=false</span></span></span></span></font></font></font></span></span></pre>

####<span style="font-variant: normal"><font color="#404040"><font face="Lato, proxima-nova, Helvetica Neue, Arial, sans-serif"><font size="3" style="font-size: 12pt"><span style="letter-spacing: normal"><span lang="en-US"><span style="font-style: normal"><span style="font-weight: normal">Direct peer to join the channel</span></span></span></span></font></font></font></span>

<pre class="western"><span style="display: inline-block; border: 1px solid #e1e4e5; padding: 0.01in"><span style="font-variant: normal"><font color="#dd1144"><font face="Consolas, Andale Mono WT, Andale Mono, Lucida Console, Lucida Sans Typewriter, DejaVu Sans Mono, Bitstream Vera Sans Mono, Liberation Mono, Nimbus Mono L, Monaco, Courier New, Courier, monospace"><font size="1" style="font-size: 7pt"><span style="letter-spacing: normal"><span lang="en-US"><span style="font-style: normal"><span style="font-weight: normal">CORE_PEER_MSPCONFIGPATH=/opt/gopath/src/github.com/hyperledger/fabric/msp/sampleconfig peer channel join -b myc1.block</span></span></span></span></font></font></font></span></span></pre>


<span style="font-variant: normal"><font color="#404040"><font face="Lato, proxima-nova, Helvetica Neue, Arial, sans-serif"><font size="3" style="font-size: 12pt"><span style="letter-spacing: normal"><span style="font-style: normal"><span style="font-weight: normal">Deploy creates the docker image for the chaincode and subsequently deploys the package to the validating peer. An example is below.</span></span></span></font></font></font></span>

<pre class="western" style="margin-bottom: 0.2in; orphans: 2; widows: 2"><span style="display: inline-block; border: 1px solid #e1e4e5; padding: 0.01in"><span style="font-variant: normal"><font color="#dd1144"><font face="Consolas, Andale Mono WT, Andale Mono, Lucida Console, Lucida Sans Typewriter, DejaVu Sans Mono, Bitstream Vera Sans Mono, Liberation Mono, Nimbus Mono L, Monaco, Courier New, Courier, monospace"><font size="1" style="font-size: 7pt"><span style="letter-spacing: normal"><span lang="en-US"><span style="font-style: normal"><span style="font-weight: normal">CORE_PEER_MSPCONFIGPATH=/opt/gopath/src/github.com/hyperledger/fabric/msp/sampleconfig peer chaincode deploy -n mycc -C myc1 -p github.com/hyperledger/fabric/examples/chaincode/go/chaincode_example02 -c '{"Args":["init","a","100","b","200"]}'</span></span></span></span></font></font></font></span></span></pre>


<span style="font-variant: normal"><font color="#404040"><font face="Lato, proxima-nova, Helvetica Neue, Arial, sans-serif"><font size="3" style="font-size: 12pt"><span style="letter-spacing: normal"><span style="font-style: normal"><span style="font-weight: normal">The response to the chaincode deploy command will contain the chaincode identifier (hash) which will be required on subsequent </span></span></span></font></font></font></span> <span style="display: inline-block; border: 1px solid #e1e4e5; padding: 0.01in"><span style="font-variant: normal"><font color="#e74c3c"><font face="Consolas, Andale Mono WT, Andale Mono, Lucida Console, Lucida Sans Typewriter, DejaVu Sans Mono, Bitstream Vera Sans Mono, Liberation Mono, Nimbus Mono L, Monaco, Courier New, Courier, monospace"><font size="2" style="font-size: 9pt"><span style="letter-spacing: normal"><span style="font-style: normal"><span style="font-weight: normal">`chaincode invoke`</span></span></span></font></font></font></span></span><span style="font-variant: normal"><font color="#404040"><font face="Lato, proxima-nova, Helvetica Neue, Arial, sans-serif"><font size="3" style="font-size: 12pt"><span style="letter-spacing: normal"><span style="font-style: normal"><span style="font-weight: normal">and</span></span></span></font></font></font></span> <span style="display: inline-block; border: 1px solid #e1e4e5; padding: 0.01in"><span style="font-variant: normal"><font color="#e74c3c"><font face="Consolas, Andale Mono WT, Andale Mono, Lucida Console, Lucida Sans Typewriter, DejaVu Sans Mono, Bitstream Vera Sans Mono, Liberation Mono, Nimbus Mono L, Monaco, Courier New, Courier, monospace"><font size="2" style="font-size: 9pt"><span style="letter-spacing: normal"><span style="font-style: normal"><span style="font-weight: normal">`chaincode query`</span></span></span></font></font></font></span></span> <span style="font-variant: normal"><font color="#404040"><font face="Lato, proxima-nova, Helvetica Neue, Arial, sans-serif"><font size="3" style="font-size: 12pt"><span style="letter-spacing: normal"><span style="font-style: normal"><span style="font-weight: normal">commands in order to uniquely identify the deployed chaincode.</span></span></span></font></font></font></span>

<span style="font-variant: normal"><font color="#404040"><font face="Roboto Slab, ff-tisa-web-pro, Georgia, Arial, sans-serif"><font size="4" style="font-size: 16pt"><span style="letter-spacing: normal"><span style="font-style: normal">**Send an invoke request**</span></span></font></font></font></span>

<pre class="western" style="margin-bottom: 0.25in; line-height: 0.25in; orphans: 2; widows: 2"><span style="display: inline-block; border: 1px solid #e1e4e5; padding: 0.01in"><span style="font-variant: normal"><font color="#dd1144"><font face="Consolas, Andale Mono WT, Andale Mono, Lucida Console, Lucida Sans Typewriter, DejaVu Sans Mono, Bitstream Vera Sans Mono, Liberation Mono, Nimbus Mono L, Monaco, Courier New, Courier, monospace"><font size="1" style="font-size: 7pt"><span style="letter-spacing: normal"><span lang="en-US"><span style="font-style: normal"><span style="font-weight: normal">CORE_PEER_MSPCONFIGPATH=/opt/gopath/src/github.com/hyperledger/fabric/msp/sampleconfig peer chaincode invoke -n mycc -C myc1 -c '{"Args":["invoke","a","b","10"]}'</span></span></span></span></font></font></font></span></span></pre>

#### <span style="font-variant: normal"><font color="#404040"><font face="Roboto Slab, ff-tisa-web-pro, Georgia, Arial, sans-serif"><font size="4" style="font-size: 16pt"><span style="letter-spacing: normal"><span style="font-style: normal">**Send a query request**</span></span></font></font></font></span>

<pre class="western" style="line-height: 0.25in; orphans: 2; widows: 2"><span style="display: inline-block; border: 1px solid #e1e4e5; padding: 0.01in"><span style="font-variant: normal"><font color="#dd1144"><font face="Consolas, Andale Mono WT, Andale Mono, Lucida Console, Lucida Sans Typewriter, DejaVu Sans Mono, Bitstream Vera Sans Mono, Liberation Mono, Nimbus Mono L, Monaco, Courier New, Courier, monospace"><font size="1" style="font-size: 7pt"><span style="letter-spacing: normal"><span lang="en-US"><span style="font-style: normal"><span style="font-weight: normal">CORE_PEER_MSPCONFIGPATH=/opt/gopath/src/github.com/hyperledger/fabric/msp/sampleconfig peer chaincode query -n mycc -C myc1 -c '{"Args":["query","a"]}'</span></span></span></span></font></font></font></span></span></pre>

**<span style="font-variant: normal"><font color="#404040"><font face="Lato, proxima-nova, Helvetica Neue, Arial, sans-serif"><font size="3" style="font-size: 12pt"><span style="letter-spacing: normal"><span style="font-style: normal">**Note:**</span></span></font></font></font></span>** <span style="font-variant: normal"><font color="#404040"><font face="Lato, proxima-nova, Helvetica Neue, Arial, sans-serif"><font size="3" style="font-size: 12pt"><span style="letter-spacing: normal"><span style="font-style: normal"><span style="font-weight: normal">If your GOPATH environment variable contains more than one element, the chaincode must be found in the first one or deployment will fail.</span></span></span></font></font></font></span>
