# mipt-db















```jsx

db.cusb.find({'Spending Score (1-100)':{$gte:50}}).explain("executionStats")
{ explainVersion: '1',
  queryPlanner: 
   { namespace: 'hw1.cusb',
     indexFilterSet: false,
     parsedQuery: { 'Spending Score (1-100)': { '$gte': 50 } },
     maxIndexedOrSolutionsReached: false,
     maxIndexedAndSolutionsReached: false,
     maxScansToExplodeReached: false,
     winningPlan: 
      { stage: 'COLLSCAN',
        filter: { 'Spending Score (1-100)': { '$gte': 50 } },
        direction: 'forward' },
     rejectedPlans: [] },
  executionStats: 
   { executionSuccess: true,
     nReturned: 25412,
     executionTimeMillis: 47,
     totalKeysExamined: 0,
     totalDocsExamined: 49999,
     executionStages: 
      { stage: 'COLLSCAN',
        filter: { 'Spending Score (1-100)': { '$gte': 50 } },
        nReturned: 25412,
        executionTimeMillisEstimate: 1,
        works: 50001,
        advanced: 25412,
        needTime: 24588,
        needYield: 0,
        saveState: 50,
        restoreState: 50,
        isEOF: 1,
        direction: 'forward',
        docsExamined: 49999 } },
  command: 
   { find: 'cusb',
     filter: { 'Spending Score (1-100)': { '$gte': 50 } },
     '$db': 'hw1' },
  serverInfo: 
   { host: 'DESKTOP-IQ3SVP0',
     port: 27017,
     version: '5.0.6',
     gitVersion: '212a8dbb47f07427dae194a9c75baec1d81d9259' },
  serverParameters: 
   { internalQueryFacetBufferSizeBytes: 104857600,
     internalQueryFacetMaxOutputDocSizeBytes: 104857600,
     internalLookupStageIntermediateDocumentMaxSizeBytes: 104857600,
     internalDocumentSourceGroupMaxMemoryBytes: 104857600,
     internalQueryMaxBlockingSortMemoryUsageBytes: 104857600,
     internalQueryProhibitBlockingMergeOnMongoS: 0,
     internalQueryMaxAddToSetBytes: 104857600,
     internalDocumentSourceSetWindowFieldsMaxMemoryBytes: 104857600 },
  ok: 1 }
  
  
  
  db.cusb.find({'Spending Score (1-100)':{$gte:50}}).explain("executionStats")
{ explainVersion: '1',
  queryPlanner: 
   { namespace: 'hw1.cusb',
     indexFilterSet: false,
     parsedQuery: { 'Spending Score (1-100)': { '$gte': 50 } },
     maxIndexedOrSolutionsReached: false,
     maxIndexedAndSolutionsReached: false,
     maxScansToExplodeReached: false,
     winningPlan: 
      { stage: 'FETCH',
        inputStage: 
         { stage: 'IXSCAN',
           keyPattern: { 'Spending Score (1-100)': 1 },
           indexName: 'Spending Score (1-100)_1',
           isMultiKey: false,
           multiKeyPaths: { 'Spending Score (1-100)': [] },
           isUnique: false,
           isSparse: false,
           isPartial: false,
           indexVersion: 2,
           direction: 'forward',
           indexBounds: { 'Spending Score (1-100)': [ '[50, inf.0]' ] } } },
     rejectedPlans: [] },
  executionStats: 
   { executionSuccess: true,
     nReturned: 25412,
     executionTimeMillis: 31,
     totalKeysExamined: 25412,
     totalDocsExamined: 25412,
     executionStages: 
      { stage: 'FETCH',
        nReturned: 25412,
        executionTimeMillisEstimate: 8,
        works: 25413,
        advanced: 25412,
        needTime: 0,
        needYield: 0,
        saveState: 25,
        restoreState: 25,
        isEOF: 1,
        docsExamined: 25412,
        alreadyHasObj: 0,
        inputStage: 
         { stage: 'IXSCAN',
           nReturned: 25412,
           executionTimeMillisEstimate: 3,
           works: 25413,
           advanced: 25412,
           needTime: 0,
           needYield: 0,
           saveState: 25,
           restoreState: 25,
           isEOF: 1,
           keyPattern: { 'Spending Score (1-100)': 1 },
           indexName: 'Spending Score (1-100)_1',
           isMultiKey: false,
           multiKeyPaths: { 'Spending Score (1-100)': [] },
           isUnique: false,
           isSparse: false,
           isPartial: false,
           indexVersion: 2,
           direction: 'forward',
           indexBounds: { 'Spending Score (1-100)': [ '[50, inf.0]' ] },
           keysExamined: 25412,
           seeks: 1,
           dupsTested: 0,
           dupsDropped: 0 } } },
  command: 
   { find: 'cusb',
     filter: { 'Spending Score (1-100)': { '$gte': 50 } },
     '$db': 'hw1' },
  serverInfo: 
   { host: 'DESKTOP-IQ3SVP0',
     port: 27017,
     version: '5.0.6',
     gitVersion: '212a8dbb47f07427dae194a9c75baec1d81d9259' },
  serverParameters: 
   { internalQueryFacetBufferSizeBytes: 104857600,
     internalQueryFacetMaxOutputDocSizeBytes: 104857600,
     internalLookupStageIntermediateDocumentMaxSizeBytes: 104857600,
     internalDocumentSourceGroupMaxMemoryBytes: 104857600,
     internalQueryMaxBlockingSortMemoryUsageBytes: 104857600,
     internalQueryProhibitBlockingMergeOnMongoS: 0,
     internalQueryMaxAddToSetBytes: 104857600,
     internalDocumentSourceSetWindowFieldsMaxMemoryBytes: 104857600 },
  ok: 1 }
```
