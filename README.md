# Weekend-Project-1-Group-5

The contract we used from here: https://github.com/Encode-Club-Solidity-Bootcamp/Lesson-04?tab=readme-ov-file#code-reference

```ruby
// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.7.0 <0.9.0;

contract HelloWorld {
    string private text;
    address public owner;

    constructor() {
        text = "Hello World";
        owner = msg.sender;
    }

    function helloWorld() public view returns (string memory) {
        return text;
    }

    function setText(string calldata newText) public onlyOwner {
        text = newText;
    }

    function transferOwnership(address newOwner) public onlyOwner {
        owner = newOwner;
    }

    modifier onlyOwner()
    {
        require (msg.sender == owner, "Caller is not the owner");
        _;
    }
}
```

deployed contract here: https://sepolia.etherscan.io/tx/0xed46f6329c0fc88efbf762a05ff1774f500ded54a2962331cc12b102fdd0fd50

![image](https://github.com/josxftd/Weekend-Project-1-Group-5/assets/129775403/60630669-4a23-481d-b929-8cdda9c18a74)

and setText to "hello Sunday morning" here: https://sepolia.etherscan.io/tx/0x506edb33c1b2bc3a670dcc6f7f296d71181066193bb372ffea16017b8519d8d3

![image](https://github.com/josxftd/Weekend-Project-1-Group-5/assets/129775403/f617da42-5bef-48fa-a1c9-849526d679de)

Seyaji provided their address (**0x4A079D4417b522762C72dB9643234FCC4683a40E**) for the transfer of ownership here: https://sepolia.etherscan.io/tx/0xa428fb3d147f1528fa7b9511e37d1dc76be7242d11a27d2224bdb1078c84d8a8

![image](https://github.com/josxftd/Weekend-Project-1-Group-5/assets/129775403/3d579b3f-6f89-454a-98d0-68d71fdd486b)
