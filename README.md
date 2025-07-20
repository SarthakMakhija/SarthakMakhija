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

- :telescope: **Princial architect, Caizin**.
- :writing_hand: Passionate about **Distributed Systems and Storage engines**. In my free time, I share my learnings on my [blog](https://tech-lessons.in/en/).
- :star: Contributed to the validation of distributed system patterns in the book [Patterns of Distributed Systems](https://learning.oreilly.com/library/view/patterns-of-distributed/9780138222246/) by Unmesh Joshi.
- :star: I authored articles on [persistent memory](https://kt.academy/article/pmem-intro) for the renowned author Marcin Moskala.
- :zap: **Personal projects**, I am building [cli-craft](https://github.com/SarthakMakhija/cli-craft/), a robust framework for building command-line interface (CLI) applications in Zig.
- :blue_book: I enjoy teaching refactoring. My preferred method for teaching refactoring involves a combination of theoretical grounding from Martin Fowler's 'Refactoring' book and hands-on practice using refactoring katas like GildedRose and TaskList. My implementations are available here: [GildedRose](https://github.com/SarthakMakhija/gilded-rose-refactoring/) and [TaskList](https://github.com/SarthakMakhija/task-list-refactoring/).
- :mailbox: Let's connect: [![Linkedin Badge](https://img.shields.io/badge/-LinkedIn-blue?style=flat&logo=Linkedin&logoColor=white)](https://www.linkedin.com/in/sarthak-makhija-7a165a55)

---

### :gear: Open-source projects

Some of my open-source project include:

[**Cli-Craft**](https://github.com/SarthakMakhija/cli-craft/)

CliCraft is a a robust framework for building command-line interface (CLI) applications in Zig. It provides a structured and idiomatic way to define commands, subcommands, flags, and arguments, ensuring a robust and user-friendly experience.

**Features**
1. **Command Parsing and Execution:** Efficiently interpret and execute commands based on user input.
2. **Parent and Child Commands:** Organize your CLI with parent and child commands, enabling clean, nested subcommands.
3. **Command Aliases:** Support for alternative command names to enhance user convenience.
4. **Flags:** Full support for defining and parsing command-line flags.
5. **Local and Persistent Flags:** Distinguish between flags scoped to a specific command and those inherited by subcommands.
6. **Typed Flags:** Built-in support for int64, bool, and string types.
7. **Short Names for Flags:** Support for single-character aliases (e.g., -v for --verbose).
8. **Arguments:** Define and validate positional arguments for your commands.
9. **Argument Specification:** Specify argument rules such as exact, minimum, or maximum count.
10. **Boolean Flags with and without Value:** Handle both implicit (--verbose) and explicit (--verbose true) boolean flag values.
11. **Flags with Default Values:** Assign default values to flags, which are used if the flag is not provided by the user.
12. **Help Command:** Automatically generated help command.
13. **Help Flag:** Automatic --help or -h flag for each command and subcommand.
14. **Robust and Tested:** Backed by extensive testing to ensure correctness and reliability..

[**Go-LSM**](https://github.com/SarthakMakhija/go-lsm)

LSM-based key-value store in Go for educational purpose.

Rewrite of the existing workshop code.

Inspired by [LSM in a Week](https://skyzh.github.io/mini-lsm/00-preface.html).

**Exploring LSM with go-lsm**
- **Learn LSM from the ground up**: Dive deep into the core concepts of Log-Structured Merge-Trees (LSM) through a practical, well-documented implementation.
- **Benefit from clean code**: Analyze a meticulously crafted codebase that prioritizes simplicity and readability.
- **Gain confidence with robust tests**: Verify the correctness and reliability of the storage engine through comprehensive tests.
- **Experiment and extend**: Customize the code to explore different LSM variations or integrate it into your own projects.

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

It has close to 2K [downloads](https://crates.io/crates/clearcheck).

[**blast**](https://github.com/SarthakMakhija/blast)

blast is a load generator for TCP servers, especially if such servers maintain persistent connections. It is implemented in golang. It is used in my current project to do the load testing of the distributed key/value storage engine that we are building.

[**CacheD**](https://github.com/SarthakMakhija/cached)

CacheD is a high performance, LFU based in-memory cache in Rust inspired by [Ristretto](https://github.com/dgraph-io/ristretto). 

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

It has close to 3K [downloads](https://crates.io/crates/tinylfu-cached).

The complete list of my side projects is available on my [blog](https://tech-lessons.in/en/page/projects/).

---

### :gear: Talks

[Questioning database claim: Design patterns of storage engines](https://github.com/SarthakMakhija/questioning-database-claims-gocon24)

I gave a talk on "Questioning database claims: Design patterns of storage engines” at GoConIndia24 on 2nd December.

The idea of the talk was to **understand various patterns of storage engines (/key-value storage engines)** like **persistence (WAL, fsync)**, **efficient retrieval (B+tree, bloom filters, data layouts)**, **efficient ingestion (Sequential IO, LSM, Wisckey)** and then **question** variety of **database claims** like **durability**, **read optimization**, **write optimization** and **pick** the **right** **database(s)** for our use case.
The recording is available [here](https://www.youtube.com/watch?v=_55OM23zhUo&list=PLbgP71NCXCqG4xkCmsn5wSpW7bhypnqHI&index=10).

### :microphone: Workshops that I conduct

  1. [**Gamifying Refactoring**](https://gamifying-refactoring.github.io/)

  I created the idea of Gamifying refactoring which is run as a game (/mini workshop) in ThoughtWorks. The idea behind this game is to identify code smells, justify each of them by going beyond ilities, finish all of this in a fixed time and win points for your team.

  2. [**Storage Engine**](https://github.com/SarthakMakhija/storage-engine-workshop)

  This hands-on workshop focusses on building a tiny LSM-tree based storage engine. It covers the basics including: Hard disks, blocks, OS page cache, encoding, decoding, endianness, basics of B+Tree and detailed internals of LSM-tree. The LSM-based storage engine code is available [here](https://github.com/SarthakMakhija/go-lsm).


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

![GitHub stats](https://github-readme-stats.vercel.app/api?username=SarthakMakhija&hide=contribs,prs,issues&show_icons=true&rank_icon=github)

![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=SarthakMakhija&layout=compact&exclude_repo=tech-lessons-posts,sarthakmakhija.github.io&langs_count=8)
---

### :writing_hand: Blog Posts

Some of my latest blogs include:

- [**Refactoring Mindset**](https://tech-lessons.in/en/blog/refactoring_mindset/)

My team and I had been reading 'Refactoring by Martin Fowler' and recently worked through the TaskList kata as a refactoring exercise. This experience inspired me to write this article, which focuses on cultivating a 'refactoring mindset' – a deliberate and proactive approach to consistently improve our code.

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


