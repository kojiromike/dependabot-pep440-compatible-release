# Test Dependabot PEP-440 Compatible Release Handling

[The compatible-release specifier in PEP 440](https://peps.python.org/pep-0440/#compatible-release) uses `~=` to declare a range of versions that is supposed to be compatible with the given version.

For example, the following groups of version clauses are equivalent:

```
~= 2.2
>= 2.2, == 2.*

~= 1.4.5
>= 1.4.5, == 1.4.*
```

But I suspect that at the time I write this, Dependabot would detect them as different and create PRs to make unnecessary updates. So I've created this repo to test it out.
