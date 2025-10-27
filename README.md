# PDC_Image_Processing


# 🧠 Parallel, Distributed & Sequential Image Processing

## 👩‍💻 Author
**Areeba Tahir**  
BS Artificial Intelligence (6th Semester)  
**COMSATS University Islamabad, Lahore Campus**

---

## 📘 Course
**Parallel and Distributed Computing (PDC)**  
Instructor: *Akhzar Nazir*  

---

## 🧩 Project Overview
This project demonstrates **Sequential**, **Parallel**, and **Distributed** image processing using Python.  
It showcases how parallelism and distributed computing can significantly reduce the total processing time for common image preprocessing tasks like **resizing** and **watermarking**.



---

## 📊 Task 4 — Performance Report (`report.txt` / `report.pdf`)

### Execution Time Comparison

| Approach        | Workers / Nodes | Time (s) | Speedup |
|-----------------|-----------------|-----------|----------|
| Sequential      | 1               | 1.92      | 1.00×    |
| Parallel        | 2 workers       | 1.05      | 1.56×    |
| Parallel        | 4 workers       | 0.48      | 3.99×    |
| Distributed Sim | 2 nodes         | 1.40      | 1.37×    |

---

### 🏆 Best Configuration
✅ **4 Parallel Workers** gave the **lowest execution time (≈ 0.48 seconds)**  
and the **highest speedup (≈ 3.99×)** over sequential processing.

Beyond 4 workers, performance gain reduced due to CPU overhead and task management cost.

---

### 💬 Discussion — Parallelism & Bottlenecks
Parallelism greatly improved performance by utilizing multiple CPU cores simultaneously.  
However, several bottlenecks limited perfect scalability:

- **Disk I/O Overhead:** Reading/writing image files still occurs sequentially.  
- **Python GIL:** Affects thread-based parallelism (though multiprocessing bypasses it).  
- **Load Imbalance:** Some processes may have slightly more work than others.  
- **Communication Cost:** Distributed nodes require synchronization and data transfer.

Despite these bottlenecks, parallel and distributed approaches clearly provided measurable performance gains over sequential execution.

---

## 🧩 Combined Summary Table

| Metric | Sequential | Parallel (4 Workers) | Distributed (2 Nodes) |
|---------|-------------|----------------------|------------------------|
| Execution Time (s) | 1.92 | 0.48 | 1.40 |
| Speedup | 1.00× | 3.99× | 1.37× |
| Best Config | – | ✅ 4 Workers | – |

---





### Example Output
