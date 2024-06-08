<div align="center">
  <div id="header">
    <img src="https://media.giphy.com/media/M9gbBd9nbDrOTu1Mqx/giphy.gif" width="100"/>
  </div>

  <div id="badges">
    <a href="https://www.linkedin.com/in/sarthak-makhija-7a165a55/">
      <img src="https://img.shields.io/badge/LinkedIn-blue?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn Badge"/>
    </a>
    <a href="https://x.com/MakhijaSarthak">
      <img src="https://img.shields.io/badge/Twitter-blue?style=for-the-badge&logo=twitter&logoColor=white" alt="Twitter Badge"/>
    </a>
  </div>

  <h1>
    hey there
    <img src="https://media.giphy.com/media/hvRJCLFzcasrR4ia7z/giphy.gif" width="30px"/>
  </h1>
</div>

### :man_technologist: About Me

- :telescope: **Software Engineer** at ThoughtWorks. Building a strongly consistent distributed Key/Value storage engine in Go.
- :writing_hand: Passionate about **Distributed Systems and Storage engines**. In my free time, I share my learnings on my [blog](https://tech-lessons.in/en/).
- :star: Contributed to the validation of distributed system patterns in the book [Patterns of Distributed Systems](https://learning.oreilly.com/library/view/patterns-of-distributed/9780138222246/) by Unmesh Joshi.
- :zap: **Personal project**, working on [LSM-tree](https://github.com/SarthakMakhija/go-lsm) based storage engine for educational purposes.
- :blue_book: I love reading books, and currently I am reading **Designing Data-Intensive Applications** by Martin Kleppmann.
- :mailbox: Let's connect: [![Linkedin Badge](https://img.shields.io/badge/-LinkedIn-blue?style=flat&logo=Linkedin&logoColor=white)](https://www.linkedin.com/in/sarthak-makhija-7a165a55)

---

### :gear: Open-source projects

Some of my open-source project include:

[**Clearcheck**](https://github.com/SarthakMakhija/clearcheck)

Write expressive and elegant assertions with ease!

clearcheck is designed to make assertion statements in Rust as clear and concise as possible.

It allows chaining multiple assertions together for a fluent and intuitive syntax, leading to more self-documenting test cases.

```rust
let pass_phrase = "P@@sw0rd1 zebra alpha";
pass_phrase.should_not_be_empty()
    .should_have_at_least_length(10)
    .should_contain_all_characters(vec!['@', ' '])
    .should_contain_a_digit()
    .should_not_contain_ignoring_case("pass")
    .should_not_contain_ignoring_case("word");
```

[**blast**](https://github.com/SarthakMakhija/blast)

blast is a load generator for TCP servers, especially if such servers maintain persistent connections. It is implemented in golang. It is used in my current project to do the load testing of the distributed key/value storage engine that we are building.

[**CacheD**](https://github.com/SarthakMakhija/cached)

CacheD is a high performance , LFU based in-memory cache in Rust inspired by Ristretto .

```rust
#[tokio::test]
async fn put_a_key_value() {
    let cached = CacheD::new(ConfigBuilder::new(COUNTERS, CAPACITY, CACHE_WEIGHT).build());
    let acknowledgement =
            cached.put("topic", "LFU cache").unwrap();
     
     let status = acknowledgement.handle().await;
     assert_eq!(CommandStatus::Accepted, status);
    
     let value = cached.get(&"topic");
     assert_eq!(Some("LFU cache"), value);
}
```

The complete list is available on my [blog](https://tech-lessons.in/en/page/projects/).

---

### :microphone: Workshops that I conduct

  1. [**Gamifying Refactoring**](https://gamifying-refactoring.github.io/)

  I created the idea of Gamifying refactoring which is run as a game (/mini workshop) in ThoughtWorks. The idea behind this game is to identify code smells, justify each of them by going beyond ilities, finish all of this in a fixed time and win points for your team.

  2. [**Storage Engine**](https://github.com/SarthakMakhija/storage-engine-workshop)

  This hands-on workshop focusses on building a tiny LSM-tree based storage engine. It covers the basics including: Hard disks, blocks, OS page cache, encoding, decoding, endianness, basics of B+Tree and detailed internals of LSM-tree. I am recreating the [LSM-tree](https://github.com/SarthakMakhija/go-lsm) based storage engine for this workshop.


---

### :hammer_and_wrench: Languages and Tools

<div>
  <img src="https://github.com/devicons/devicon/blob/master/icons/go/go-original-wordmark.svg" title="Go" alt="Go" width="40" height="40"/>&nbsp;
  <img src="https://github.com/devicons/devicon/blob/master/icons/rust/rust-original.svg" title="Rust" alt="Rust" width="40" height="40"/>&nbsp;
  <img src="https://github.com/devicons/devicon/blob/master/icons/java/java-original-wordmark.svg" title="Java" alt="Java" width="40" height="40"/>&nbsp;
  <img src="https://github.com/devicons/devicon/blob/master/icons/kotlin/kotlin-original-wordmark.svg" title="Kotlin" alt="Kotlin" width="40" height="40"/>&nbsp;
  <img src="https://github.com/devicons/devicon/blob/master/icons/postgresql/postgresql-original-wordmark.svg" title="PostgreSQL" alt="PostgreSQL" width="40" height="40"/>&nbsp;
  <img src="https://github.com/devicons/devicon/blob/master/icons/rocksdb/rocksdb-original.svg" title="RocksDB" alt="RocksDB" width="40" height="40"/>&nbsp;
  <img src="https://github.com/devicons/devicon/blob/master/icons/docker/docker-original-wordmark.svg" title="Docker" alt="Docker" width="40" height="40"/>&nbsp;
  <img src="https://github.com/devicons/devicon/blob/master/icons/git/git-plain-wordmark.svg" title="Git" alt="Git" width="40" height="40"/>&nbsp;  
</div>

---

### :fire: My Stats

[![GitHub Streak](https://github-readme-streak-stats.herokuapp.com?user=SarthakMakhija)](https://git.io/streak-stats)
<br/>
![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=SarthakMakhija&layout=compact&exclude_repo=tech-lessons-posts,sarthakmakhija.github.io)

---

### :writing_hand: Blog Posts

Some of my latest blogs include:

- [**Many flavors of Networking IO**](https://tech-lessons.in/en/blog/many_flavors_of_networking_io/)

The foundation of any networked application hinges on its ability to efficiently handle data exchange. But beneath the surface, there’s a hidden world of techniques for managing this communication. This article dives into various “flavors” of networking IO, exploring the trade-offs associated with each approach.
To illustrate various ways applications handle network traffic, we’ll build a TCP server using four distinct approaches: blocking I/O with a single thread, blocking I/O with multiple threads, non-blocking I/O with busy waiting, and a single-threaded event loop.
Each approach offers unique advantages and drawbacks, and by constructing a server for each approach, we’ll gain a deeper understanding of their strengths and weaknesses.

- [**Serializable Snapshot Isolation**](https://tech-lessons.in/en/blog/serializable_snapshot_isolation/)

Ensuring data consistency in the face of concurrent transactions is a critical challenge in database management. 
Traditional serializable isolation, while guaranteeing data integrity, often suffers from performance bottlenecks due to extensive locking. 
This article explores Serializable Snapshot Isolation (SSI) that promises the best of both worlds: strong data consistency without sacrificing performance. 
The article delves into the inner workings of SSI and explore its implementation for a Key/Value storage engine. I will refer to the research paper titled A critique of snapshot isolation .

- [**Cache-Line Hash Table**](https://tech-lessons.in/en/blog/cache_line_hash_table/)
  
In the world of multi-core processors, managing concurrent access to data structures is crucial for efficient performance. But frequent updates can trigger a hidden bottleneck: cache coherence traffic.
This traffic arises when one core modifies the data another core has cached, forcing updates and invalidation across the system.
This article dives into a clever solution: the Cache-Line Hash Table (CLHT). CLHTs are specifically designed to minimize this cache coherence traffic, boosting the speed of concurrent data access.
We’ll explore the core ideas behind CLHTs, including:

  - **One Bucket Per CPU Cache-Line**: By cleverly aligning buckets with CPU cache line sizes, CLHTs minimize the number of lines written during updates.
  - **In-Place Updates**: Instead of shuffling data around, CLHTs update key-value pairs directly within the bucket, reducing memory movement.
  - **Lock-Free Reads**: Reads are designed to be lock-free, meaning they can proceed without acquiring locks, further enhancing performance.


