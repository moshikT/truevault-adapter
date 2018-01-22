# TrueVault-Adapter

TrueVault controller/adapter for handling request to trueVault api.

 * Includes support for session store implementation

Example:

const TrueVault = require('truevault-adapter');

// Get a list of documents
TrueVault.getDocumentsByIds(arrayOfDocumentsIds)
            .then(documents => {
                console.log(documents);
            })
            .catch (error => {
                console.log(error);
            })

// Read document
TrueVault.getDocumentById(documentId)
            .then(documentData => {
                console.log(documentData);
            })
            .catch (error => {
                console.log(error);
            })

// Creates new document
TrueVault.saveDocument(documentData)
            .then(documentId => {
                console.log(documentId);
            })
            .catch (error => {
                console.log(error);
            })

// Updates existing document
TrueVault.saveDocument(documentData, documentId)
            .then(documentId => {
                console.log(documentId);
            })
            .catch (error => {
                console.log(error);
            })

// Get user data
TrueVault.getUser(accessToken)
            .then(documentId => {
                console.log(userData);
            })
            .catch (error => {
                console.log(error);
            })
