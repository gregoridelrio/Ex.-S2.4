1. ## 📊 Query Performance Report

- 🧪 **Query**: `db.restaurants.find({}, { "_id": 0 })`
- ⏱️ **Execution time**: 0 ms
- 📚 **Documents returned**: 664
- 🔍 **Documents examined**: 664
- 🛠️ **Execution stage**: PROJECTION_SIMPLE

## ✅ No significant issues detected


2. ## 📊 Query Performance Report

- 🧪 **Query**: `db.restaurants.find({}, { "restaurant_id": 1, "name": 1, "_id": 0 })`
- ⏱️ **Execution time**: 1 ms
- 📚 **Documents returned**: 664
- 🔍 **Documents examined**: 664
- 🛠️ **Execution stage**: PROJECTION_SIMPLE

## 🚨 Performance Issues

### ℹ️ Recommendations
- ‼️ Filtering on unindexed field 'name' - performance may suffer.

### 💡 Suggested Indexes
Consider creating these indexes:
```javascript
db.restaurants.createIndex({ name: 1 });
```


3. ## 📊 Query Performance Report

- 🧪 **Query**: `db.restaurants.find({}, { "restaurant_id": 1, "name": 1, "borough" : 1, "cuisine": 1, "_id": 0 })`
- ⏱️ **Execution time**: 0 ms
- 📚 **Documents returned**: 664
- 🔍 **Documents examined**: 664
- 🛠️ **Execution stage**: PROJECTION_SIMPLE

## 🚨 Performance Issues

### ℹ️ Recommendations
- ‼️ Filtering on unindexed field 'borough' - performance may suffer.
- ‼️ Filtering on unindexed field 'cuisine' - performance may suffer.
- ‼️ Filtering on unindexed field 'name' - performance may suffer.

### 💡 Suggested Indexes
Consider creating these indexes:
```javascript
db.restaurants.createIndex({ borough: 1 });
db.restaurants.createIndex({ cuisine: 1 });
db.restaurants.createIndex({ name: 1 });
```


4. ## 📊 Query Performance Report

- 🧪 **Query**: `db.restaurants.find({}, { "restaurant_id": 1, "name": 1, "borough" : 1, "address.zipcode": 1, "_id": 0 })`
- ⏱️ **Execution time**: 0 ms
- 📚 **Documents returned**: 664
- 🔍 **Documents examined**: 664
- 🛠️ **Execution stage**: PROJECTION_DEFAULT

## 🚨 Performance Issues

### ℹ️ Recommendations
- ‼️ Filtering on unindexed field 'borough' - performance may suffer.
- ‼️ Filtering on unindexed field 'name' - performance may suffer.

### 💡 Suggested Indexes
Consider creating these indexes:
```javascript
db.restaurants.createIndex({ borough: 1 });
db.restaurants.createIndex({ name: 1 });
```


