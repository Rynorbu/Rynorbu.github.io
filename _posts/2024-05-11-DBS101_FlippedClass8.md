---
Title: DBS101 Flipped Class8
categories: [DBS101, Flipped_class8]
tags: [DBS101]
---
## Topic: Indexing
---
![alt text](../flip8/hello.gif)

Hello everyone, Hope you are doing well. Today we will discuss the topic of Indexing and Its types.

Before explaining the types of Indexing, let's first understand what Indexing is.

Indexing is a data structure that improves the speed of data retrieval operations on a database table at the cost of additional writes and storage space to maintain the index data structure.

### Types of Indexing:

### Buffer Tree

A Buffer Tree, also called a B-Tree, is a data structure used to efficiently store and manage large amounts of data, such as audio or video files.
* It keeps everything neat and sorted so that finding, adding, or removing stuff is  quick and easy. 
* It is like a super organized system that makes searching, adding, and deleting data super fast, whether it's in a computer database or managing files on a computer's storage.
* It's called a tree because it's made up of nodes that are connected like branches on a tree.

![alt text](../flip8/buffer.png)

#### How does a buffer tree work?

Firstly, the buffer tree divides the data into smaller, more manageable chunks called "buffers."

Then these buffers are then organized into a tree-like structure, with each buffer stored in a node of the tree.

The tree is designed to be balanced, meaning that the height of the tree is kept as low as possible, which makes it faster to access the data.

#### How the buffer tree is used

* They are used in multimedia applications, such as video and audio players, to manage the storage and playback of large media files.

* They are also used in file systems and database management systems to efficiently store and retrieve large amounts of data.

#### Advantages of a buffer tree

1. Efficient storage: By breaking the data into smaller chunks and storing them in a balanced tree, the buffer tree can store large amounts of data more efficiently.

2. Fast data access: The tree-like structure of the buffer tree allows for quick and easy access to specific parts of the data, without having to read through the entire file.

3. Scalability: As the amount of data grows, the buffer tree can be easily expanded to accommodate the new data, without impacting the performance.

### Bitmap Indexing









