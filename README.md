# TrueVault-Adapter

TrueVault controller/adapter for handling request to trueVault api.

 * Includes support for session store implementation

## Example:

```javascript
const TrueVault = require('truevault-adapter')();

// initialize params
const params = {
    apiKey: "<API_KEY>", // base64 encoded
    vaultId: '<VAULT_ID>',
    collectionSchemaId: "<COLLECTION_SCHEMA_ID>",
    sessionSchemaId: "<SESSION_COLLECTION_SCHEMA_ID>" // Optional
};

const truevault  = new TrueVault(params);


// Get a list of documents
truevault.getDocumentsByIds(arrayOfDocumentsIds)
            .then(documents => {
                console.log(documents);
            })
            .catch (error => {
                console.log(error);
            })

// Read document
truevault.getDocumentById(documentId)
            .then(documentData => {
                console.log(documentData);
            })
            .catch (error => {
                console.log(error);
            })

// Creates new document
truevault.saveDocument(documentData)
            .then(documentId => {
                console.log(documentId);
            })
            .catch (error => {
                console.log(error);
            })

// Updates existing document
truevault.saveDocument(documentData, documentId)
            .then(documentId => {
                console.log(documentId);
            })
            .catch (error => {
                console.log(error);
            })

// Get user data
truevault.getUser(accessToken)
            .then(userData => {
                console.log(userData);
            })
            .catch (error => {
                console.log(error);
            })
```
