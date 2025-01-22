# Codtech-Task-2

Name:Rohith Jairaam .P.c
ID:CT08HKX
Domain:c++ programming 
Duration:December 30th, 2024 to January 30th, 2025
Mentor:

# Overview of C++ programming (MULTITHREADEDFILE COMPRESSION TOOL) 

1. The program compresses and decompresses files using multithreading and the zlib library.  
2. It reads files in chunks to optimize performance and memory usage.  
3. The program supports two modes: `"compress"` and `"decompress"`.  
4. It processes data in 1 MB chunks to handle large files efficiently.  
5. Each chunk is processed by a separate thread for parallelism.  
6. The `std::vector<char>` is used to store input and output data for each chunk.  
7. **Compression**:
   - Uses the `compress()` function from zlib to compress chunks.
   - The compressed size is calculated dynamically using `compressBound()`.  
8. **Decompression**:
   - Uses the `uncompress()` function from zlib to decompress chunks.
   - Assumes a maximum decompression ratio for initial buffer size.  
9. A `std::mutex` ensures thread-safe writing to the output file.  
10. Threads are managed dynamically and joined after processing each chunk.  
11. The `processFile()` function handles both compression and decompression.  
12. Files are opened in binary mode using `std::ifstream` and `std::ofstream`.  
13. If files fail to open, an error message is displayed.  
14. Each chunk of data is read from the input file, processed, and written to the output file.  
15. The program terminates processing when all chunks are completed.  
16. Handles edge cases like zero-byte files and invalid file paths.  
17. The `main()` function parses command-line arguments for mode, input, and output files.  
18. The mode determines whether to compress or decompress the file.  
19. If an invalid mode is entered, an error message is shown.  
20. If no errors occur, the program prints a success message upon completion.  
21. Designed for efficient multithreading with minimal contention.  
22. Requires zlib library and C++11 or later for compilation.  
23. Provides a fast and scalable way to compress and decompress large files.  
