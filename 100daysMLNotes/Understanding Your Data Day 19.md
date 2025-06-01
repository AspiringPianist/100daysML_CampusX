1. How Big is the Data
```python
df.shape
```
2. How does the data look like
```python
df.head() or df.sample(5)
```
3. What is the data type of cols
```python
df.info()
```
4. Are there any missing values?
```python
df.isnull().sum()
```
5. How does data look mathematically?
```python
df.describe()
```
6. Are there duplicate values?
```python
df.duplicated().sum()
```
7. How is the correlation between cols (only numerical ones)
```python
df.corr()
df.corr()['Survived']
```
