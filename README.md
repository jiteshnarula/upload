# upload
upload


using sets

//Base class
class Product {

    //constructor function
    constructor(productID, productName, productPrice, productDescription) {
        this.productID = productID;
        this.productName = productName;
        this.productPrice = productPrice;
        this.productDescription = productDescription;
    }
    printAllProducts() {
        let productDetails =
            `Product ID: ${this.productID}
        Product Name: ${this.productName}
        Product Price: ${this.productPrice}
        Product Description: ${this.productDescription}`
        return productDetails;
    }
}
class Product1 extends Product {

    constructor(productID, productName, productPrice, productDescription, productType) {
        super(productID, productName, productPrice, productDescription);
        this.productType = productType;

    }

    printAllProducts() {
        let allProducts = `${super.printAllProducts()}+
                                Product Type :  + ${this.productType} `
        return allProducts;
    }
}

class Product2 extends Product {

    constructor(productID, productName, productPrice, productDescription
        , productCategory) {
        super(productID, productName, productPrice, productDescription);
        this.productCategory = productCategory;

    }

    printAllProducts() {
        let allProducts = `${super.printAllProducts()}+
                                Product Category :  + ${this.productCategory} `
        return allProducts;
    }
}







var productObj1 = new Product1(2, "Jitesh", 100000, "Capgemini", "Salty");
console.log(productObj1.printAllProducts());

var productObj2 = new Product2(1, "Jites3", 10000, "Capgemini2", "Eggg");
console.log(productObj2.printAllProducts());


var productObj3 = new Product1(3, "Sahil", 100000, "Capgemini", "Salty");
console.log(productObj1.printAllProducts());

var productObj4 = new Product2(4, "Paras", 10000, "Capgemini2", "Eggg");
console.log(productObj2.printAllProducts());


// let allProducts = [];
let allProducts = new Set();
allProducts.add(productObj1);
allProducts.add(productObj2);

allProducts.add(productObj3);
allProducts.add(productObj4);


for(var product of allProducts){
    console.log(product.printAllProducts());
}

console.log("After sorting in ascending order");

let sortedSet = Array.from(allProducts).sort((a,b)=> 
            a.productID - b.productID);


for(var product of sortedSet){
    console.log(product.printAllProducts());
}


// console.log("Updating with Find Method.....");

// let productId = parseInt(prompt("Enter product id"));

// let updateProduct = 
//     Array.from(allProducts).find(p=> p.productID === productId);
//     updateProduct.productName = "Lenovo"


//     for(var product of updateProduct){
//         console.log(updateProduct[product].printAllProducts());
//     }
    



    console.log("deleted Product");
    let productId = parseInt(prompt("Enter product id"));

let deletedProduct = 
    Array.from(allProducts).find(p=> p.productID === productId);
    allProducts.delete(deletedProduct);


    for(var product of allProducts){
        console.log(product.printAllProducts());
    }
    

// console.log("Updating.... ");
// let productId = parseInt(prompt("Enter product id"));
// for(var product of allProducts){
//     if(product.productID === productId){
//         product.productName = "Delll";
//     }
// }


// for (var product in allProducts) {
//     console.log(allProducts[product].printAllProducts());
// }


// let productId = parseInt(prompt("Enter product id"));

// for (var product in allProducts) {
    
//     if (allProducts[product].productID == productId) {

//         allProducts[product].productName = "JiteshNarula";
//         console.log("After Updating.... ")


//         for (var product in allProducts) {
//             console.log(allProducts[product].printAllProducts());
//         }


//     }  

// }



// let productid2 = prompt("Enter Product ID");
 
// for(var product in allProducts){
//     if(allProducts[product].productID == productid2 ){
//          allProducts.splice(product,1);
//         }
// }


// console.log("After Deleting.... ")


// for (var product in allProducts) {
//     console.log(allProducts[product].printAllProducts());
// }




















using array


//Base class
class Product {

    //constructor function
    constructor(productID, productName, productPrice, productDescription) {
        this.productID = productID;
        this.productName = productName;
        this.productPrice = productPrice;
        this.productDescription = productDescription;
    }
    printAllProducts() {
        let productDetails =
            `Product ID: ${this.productID}
        Product Name: ${this.productName}
        Product Price: ${this.productPrice}
        Product Description: ${this.productDescription}`
        return productDetails;
    }
}
class Product1 extends Product {

    constructor(productID, productName, productPrice, productDescription, productType) {
        super(productID, productName, productPrice, productDescription);
        this.productType = productType;

    }

    printAllProducts() {
        let allProducts = `${super.printAllProducts()}+
                                Product Type :  + ${this.productType} `
        return allProducts;
    }
}

class Product2 extends Product {

    constructor(productID, productName, productPrice, productDescription
        , productCategory) {
        super(productID, productName, productPrice, productDescription);
        this.productCategory = productCategory;

    }

    printAllProducts() {
        let allProducts = `${super.printAllProducts()}+
                                Product Category :  + ${this.productCategory} `
        return allProducts;
    }
}







var productObj1 = new Product1(2, "Jitesh", 100000, "Capgemini", "Salty");
console.log(productObj1.printAllProducts());

var productObj2 = new Product2(1, "Jites3", 10000, "Capgemini2", "Eggg");
console.log(productObj2.printAllProducts());


var productObj3 = new Product1(3, "Sahil", 100000, "Capgemini", "Salty");
console.log(productObj1.printAllProducts());

var productObj4 = new Product2(4, "Paras", 10000, "Capgemini2", "Eggg");
console.log(productObj2.printAllProducts());


let allProducts = [];
allProducts.push(productObj1);
allProducts.push(productObj2);

allProducts.push(productObj3);
allProducts.push(productObj4);


for(var product in allProducts){
    console.log(allProducts[product].printAllProducts());
}

console.log("After sorting in ascending order");

allProducts.sort((a,b)=> a.productID - b.productID);


for(var product in allProducts){
    console.log(allProducts[product].printAllProducts());
}


// for (var product in allProducts) {
//     console.log(allProducts[product].printAllProducts());
// }


// let productId = parseInt(prompt("Enter product id"));

// for (var product in allProducts) {
    
//     if (allProducts[product].productID == productId) {

//         allProducts[product].productName = "JiteshNarula";
//         console.log("After Updating.... ")


//         for (var product in allProducts) {
//             console.log(allProducts[product].printAllProducts());
//         }


//     }  

// }



// let productid2 = prompt("Enter Product ID");
 
// for(var product in allProducts){
//     if(allProducts[product].productID == productid2 ){
//          allProducts.splice(product,1);
//         }
// }


// console.log("After Deleting.... ")


// for (var product in allProducts) {
//     console.log(allProducts[product].printAllProducts());
// }




//maps





//Base class
class Product {

    //constructor function
    constructor(productID, productName, productPrice, productDescription) {
        this.productID = productID;
        this.productName = productName;
        this.productPrice = productPrice;
        this.productDescription = productDescription;
    }
    printAllProducts() {
        let productDetails =
            `Product ID: ${this.productID}
        Product Name: ${this.productName}
        Product Price: ${this.productPrice}
        Product Description: ${this.productDescription}`
        return productDetails;
    }
}
class Product1 extends Product {

    constructor(productID, productName, productPrice, productDescription, productType) {
        super(productID, productName, productPrice, productDescription);
        this.productType = productType;

    }

    printAllProducts() {
        let allProducts = `${super.printAllProducts()}+
                                Product Type :  + ${this.productType} `
        return allProducts;
    }
}

class Product2 extends Product {

    constructor(productID, productName, productPrice, productDescription
        , productCategory) {
        super(productID, productName, productPrice, productDescription);
        this.productCategory = productCategory;

    }

    printAllProducts() {
        let allProducts = `${super.printAllProducts()}+
                                Product Category :  + ${this.productCategory} `
        return allProducts;
    }
}







var productObj1 = new Product1(2, "Jitesh", 100000, "Capgemini", "Salty");
console.log(productObj1.printAllProducts());

var productObj2 = new Product2(1, "Jites3", 10000, "Capgemini2", "Eggg");
console.log(productObj2.printAllProducts());


var productObj3 = new Product1(3, "Sahil", 100000, "Capgemini", "Salty");
console.log(productObj1.printAllProducts());

var productObj4 = new Product2(4, "Paras", 10000, "Capgemini2", "Eggg");
console.log(productObj2.printAllProducts());


// let allProducts = [];
let allProducts = new Map();
allProducts.set(1,productObj1);
allProducts.set(2,productObj2);

allProducts.set(3,productObj3);
allProducts.set(4,productObj4);


for(var [k,v] of allProducts){
    console.log(allProducts.get(k).printAllProducts());
}

// console.log("After sorting in ascending order");

// let sortedSet = Array.from(allProducts).sort((a,b)=> 
//             a[1].productID - b[1].productID);

//             for(var [k,v] of sortedSet){
//                 console.log(allProducts.get(k).printAllProducts());
//             }

console.log("Updating with Find Method.....");

let productId = parseInt(prompt("Enter product id"));

let updateProduct = 
    Array.from(allProducts).find(p => p[1].productID === productId);
    updateProduct[1].productName = "Lenovo"


    for(var [k,v] of updateProduct){
        console.log(allProducts.get(k).printAllProducts());
        }
    



//     console.log("deleted Product");
//     let productId = parseInt(prompt("Enter product id"));

// let deletedProduct = 
//     Array.from(allProducts).find(p=> p[1].productID === productId);
//     allProducts.delete(deletedProduct[0]);


   
//     for(var [k,v] of allProducts){
//         console.log(allProducts.get(k).printAllProducts());
//     }
// console.log("Updating.... ");
// let productId = parseInt(prompt("Enter product id"));
// for(var product of allProducts){
//     if(product.productID === productId){
//         product.productName = "Delll";
//     }
// }


// for (var product in allProducts) {
//     console.log(allProducts[product].printAllProducts());
// }


// let productId = parseInt(prompt("Enter product id"));

// for (var product in allProducts) {
    
//     if (allProducts[product].productID == productId) {

//         allProducts[product].productName = "JiteshNarula";
//         console.log("After Updating.... ")


//         for (var product in allProducts) {
//             console.log(allProducts[product].printAllProducts());
//         }


//     }  

// }



// let productid2 = prompt("Enter Product ID");
 
// for(var product in allProducts){
//     if(allProducts[product].productID == productid2 ){
//          allProducts.splice(product,1);
//         }
// }


// console.log("After Deleting.... ")


// for (var product in allProducts) {
//     console.log(allProducts[product].printAllProducts());
// }
