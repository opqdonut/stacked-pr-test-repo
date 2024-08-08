Surprising behaviour with stacked PRs.

1. Create two commits in sequence on top of main: main--A--B
2. Create a PR for commit A: [#1](https://github.com/opqdonut/stacked-pr-test-repo/pull/1)
3. Create a PR for commit B: [#2](https://github.com/opqdonut/stacked-pr-test-repo/pull/2)
    – shows both commits A and B
    - this is correct, in my opinion: merging #2 would add both commits to main
4. Merge PR A
5. PR B still shows commits A and B
    - this is wrong, in my opinion: A has already been merged and merging this PR won't include it
6. Create a new PR for commit B: [#3](https://github.com/opqdonut/stacked-pr-test-repo/pull/3)
    – now shows only commit B!
    - this is correct but new behaviour AFAIK – I don't think the PR creation time affected the contents previously
