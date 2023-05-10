# sway-git-checkout-bug-repro

To repro, try building the project using `forc build`

Here are my logs:

```
sway-git-checkout-bug-repro on  main 
❯ forc build
  WARNING! unused manifest key: project.target
  WARNING! unused manifest key: project.target
  WARNING! unused manifest key: project.target
  WARNING! unused manifest key: project.target
  WARNING! unused manifest key: project.target
  WARNING! unused manifest key: project.target
  WARNING! unused manifest key: constants
  WARNING! unused manifest key: constants
 Compiling library core (/Users/dhaiwat/.forc/git/checkouts/std-77214b14e13f9b04/a11538053fd815f92d0374543ab40a975fa23dbd/sway-lib-core)
error
 --> /Users/dhaiwat/.forc/git/checkouts/std-77214b14e13f9b04/a11538053fd815f92d0374543ab40a975fa23dbd/sway-lib-core/src/lib.sw:3:1
  |
1 | 
2 | 
3 | pub mod primitives;
  | ^^^ Unnecessary visibility qualifier, `pub` is implied here.
4 | pub mod raw_ptr;
5 | pub mod raw_slice;
  |
____

error
 --> /Users/dhaiwat/.forc/git/checkouts/std-77214b14e13f9b04/a11538053fd815f92d0374543ab40a975fa23dbd/sway-lib-core/src/lib.sw:4:1
  |
2 | 
3 | pub mod primitives;
4 | pub mod raw_ptr;
  | ^^^ Unnecessary visibility qualifier, `pub` is implied here.
5 | pub mod raw_slice;
6 | pub mod ops;
  |
____

error
 --> /Users/dhaiwat/.forc/git/checkouts/std-77214b14e13f9b04/a11538053fd815f92d0374543ab40a975fa23dbd/sway-lib-core/src/lib.sw:5:1
  |
3 | 
4 | pub mod raw_ptr;
5 | pub mod raw_slice;
  | ^^^ Unnecessary visibility qualifier, `pub` is implied here.
6 | pub mod ops;
7 | pub mod never;
  |
____

error
 --> /Users/dhaiwat/.forc/git/checkouts/std-77214b14e13f9b04/a11538053fd815f92d0374543ab40a975fa23dbd/sway-lib-core/src/lib.sw:6:1
  |
4 | 
5 | pub mod raw_slice;
6 | pub mod ops;
  | ^^^ Unnecessary visibility qualifier, `pub` is implied here.
7 | pub mod never;
8 | pub mod r#storage;
  |
____

error
 --> /Users/dhaiwat/.forc/git/checkouts/std-77214b14e13f9b04/a11538053fd815f92d0374543ab40a975fa23dbd/sway-lib-core/src/lib.sw:7:1
  |
5 | 
6 | pub mod ops;
7 | pub mod never;
  | ^^^ Unnecessary visibility qualifier, `pub` is implied here.
8 | pub mod r#storage;
9 | pub mod prelude;
  |
____

error
 --> /Users/dhaiwat/.forc/git/checkouts/std-77214b14e13f9b04/a11538053fd815f92d0374543ab40a975fa23dbd/sway-lib-core/src/lib.sw:8:1
  |
6 | 
7 | pub mod never;
8 | pub mod r#storage;
  | ^^^ Unnecessary visibility qualifier, `pub` is implied here.
9 | pub mod prelude;
  |
____

error
 --> /Users/dhaiwat/.forc/git/checkouts/std-77214b14e13f9b04/a11538053fd815f92d0374543ab40a975fa23dbd/sway-lib-core/src/lib.sw:9:1
  |
7 | 
8 | pub mod r#storage;
9 | pub mod prelude;
  | ^^^ Unnecessary visibility qualifier, `pub` is implied here.
  |
____

  Aborting due to 7 errors.
Error: Failed to compile core
```
