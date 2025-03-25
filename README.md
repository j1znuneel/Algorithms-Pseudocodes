# Algorithms-Pseudocodes

## Merge Sort Algorithm

```jsx
MergeSort(A[0...n-1]):
	if n>1:
		copy A[0...n/2 -1] to B[0...n/2 -1]
		copy A[n/2...n-1] to C[0...n/2 -1] 
		MergeSort(B[0...n/2 -1]
		MergeSort(C[0...n/2 -1]
		Merge(B,C,A)
	
	
Merge(B[0...p-1],C[0...q-1],A[0...p+q-1]):
	i=0
	j=0
	k=0
	while i<p and j<q
		if(B[i]<=C[j]):
			A[k]=B[i]
			i++
		else:
			A[k]=C[j]
			j++
		k++
	if i==p:
		copy C[j...q-1] to A[k...p+q-1]
	else:
		copy B[i...p-1] to A[k...p+q-1]
```

## Quick Sort

```jsx
QuickSort(A[lb,ub]):
	loc=Partition(A,lb,ub)
	QuickSort(A[lb,loc-1])
	QuickSort(A[loc+1,ub])
	
Partition(A,lb,ub):
	pivot=A[lb]
	start=lb
	end=ub
	while start<end:
		while A[start]<=pivot:
			start++
		while A[end]>pivot:
			end--
		if start<end:
			swap(A[start],A[end])
	swap(pivot and A[end]
```

## Binary Search

```jsx
BinarySearch(A[0...n-1],K):
	while(l<=r) do:
			m=l+r/2
			if(K==A[m]):
				return m
			else if(k<=A[m])
				r=m-1
			else:
				l=m+1
	return -1
```

## Selection Sort

```jsx
SelectionSort(A):
	for(i=0 to n-2):
		min=i
		for(j=i+1 to n-1):
			if(A[j]<A[i]):
				min=j
		swap A[i] & A[min]
```

## Bubble Sort

```jsx
BubbleSort(A):
	for(i=0 to n-2):
		for(j=0 to n-2-i):
			if(A[j]>A[j+1]):
				swap A[j] & A[j+1])
				
				
```

## Sequential Search

```jsx
SequentialSearch(A):
	A[n]=k
	i=0
	while A[i]!=k:
		i++
		
	if(i<n):
		return i
	else:
		return -1

```

## Bruteforce String Matching

```jsx
for i=0 to n-m:
	j=0
	while j<m and P[j]==T[i+j]:
		j++;
	if j==m:
		return i

return -1
```

# Dynamic Programming

- Introduced to solve problems with overlapping subproblems
- Instead of solving overlapping subproblems again and again DP stores it in a table and reuses when necessary

## Coin Row Problem

```jsx
CRP(C[1...n]):
	F[0]=0
	F[1]=C[1]
	for i=2 to n,do:
		F[i]=MAX{C[i]+F[i-2],F[i-1]}
	return F[n]
```
