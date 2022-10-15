# AuthLink

Locked links.

Try it out:

(Right-click: open in new tab. Because GitHub's readme won't open it in a new tab.)

Follow: [public link](https://konelinx.be/authlink/#salt=tmzbf4emxqgEbY0IVkoX6c1Bz3FoSo5k6YaeQobjonG2pHjFz/Zl7rfvAQhlv61cAvk0/mjGiXmY6ybwu+6ykQ==#id=d6WmSNkbbyMUuZJZY+IWvKN6irTktGba+pv4cFBVttgTc+oqLtmeNywm6Qs2XWgxEt3GxSp19tJnV5+fx59k90fatH5qpoX3BBb4rlSyLMhdm6roo/zYQ4Aaz+hgOWLLBR7/incKbB2rbTQVbyCXsQFiwzYxq4wz6xd8MRvmYWcct8gl9MEzFzmLAYeyGVhrl+13T4Cf4VnESurRztqy94zCtH82euFVXaR4fwEVoZAdjCcLIdaR7m8pNot78Ul1eorVMfJvDVYnNwJ0WztUGlAHr42LqR4e1CMIJh8lTFBXLB/boPDR6lF3X9IPD9Hg3+iqfh5dq1m3O5P1AysoK5cIkV//mTDdi34XPUdrGbgL7R9jZeCclMXtTFy+u0gJFvgtNfdwiuTSGHrBh8UlIm46a9DIT0bTXH3kLhzSEfhnhPhJYN/EQWAtU81iLnlHdykaFf5eQWrl2jxCckVchfdpyCJ2BzHGfHrKucDF6RE8zEXbQtUPNdc06afJcDy0fIQbYA6f6bLO13EJ10TSE70tuvP7yz2hPGNeyRsMwTiNCJMWDCwLER2mEvAromR+BTi9PULf6n6jIT/gYE5bMPIxwRvnyi7ofqkAfBA5fA4aneGyvXJtOAaVuY5DZ5nDIa8/O8RuDesTGKl4Hf734vj+lf+oTv6F07+wEPPM2Mc=#url#type=image/jpeg##jFOdU8yzO7OPuqEhSTHPlCbh0dt0l/jC0jPhTQAXoFHEQd8FgfabvGkqS7o10LTY0T9n7cyRC2EehBCiScKgoq60Jpb4B6I5rCrgwTDj7UGCiFVT5NVUSKPlHTjf9hRkCl+q2V67tfeLgM8KVQ==)
\> Follow: [private link](https://konelinx.be/authlink/#key=MIICIjANBgkqhkiG9w0BAQEFAAOCAg8AMIICCgKCAgEA1VkC7rsca4RCXU78yOlLQ9LLBfQN5PmpRovId7BNHOAkuBr1gpC7vcFxkdo5H/tilDx480Q8efd463ooHeKfYFB8sFDa6UmPQ693aZvzJHcUEPhpv+B/U6fWwNlldWkWwqhjOHwC17A7C2eVvMLM092tS62ewuNN9HYTmXllCyakJuj+LhalxRqBAiMJiKgVxuXnFURRKMpr5QXPJOe1vwYLJiWOryJ51UFShyVKmRyB9+9et7EH+VQRIFih5V0dcdZEL1B7nmbyXY6fMnOxYWlNwy+bSvAWC7e11TRhlpnF50N/7YJ2WFUJEWWZk0qfrScaCqMxKpBSRV+g3Tyytpxx3e2hTK2cBe/a5sCYC8a4sFSuA1Pz53Qqxkf/dfMv0uBfLfmlifw/aSEHO/5t85TBHQ/1QwyUZgmIwnAqn2wf8v+MV6c6lj3apIh4keyQ31C3+fVwtr5K28WEbU6EiYNxawUxbYGY87hYU/URlp2cvGkgPwoe/aLPC59UuHS3Py2kBxMUsmn5NV/LcF4NJBIZaOAzfSjJQ8Rn6LYyCRnbo8Hk6X5nXFGLgd/Q+3nvANoX2eAoOfJ66A2nf7t3YC1U8HNqD7ZAi6Lv+d0rpdtH+LJzb/4nup4WhHUbrKWwwUk7PYJ6/oLD/p/6PL2lYPkDrOxZ207oBWhb14gZ+GsCAwEAAQ==)
\> Now follow the public link again.

This page is loading a third party [resource](https://konelinx.be/authlink/testfile01.txt) that has been encrypted and decrypts it on the fly at the client. As can be seen it has little issue decrypting a 2MB file.

## How to use

The page can be loaded with a hash consisting of parameters seperated by a hash tag. the final parameter containing the data is preceded with a double hash tag. E.g. the tags create, type and the attached data `#create##Hello%20world!`.

### create a link

Load the page with a hash containing `create` to create a link pair.

```
#create##Hello%20world!
```

This will create a provate and a piblic link. The private link contains the key: share this key with sources you trust. The public link is the sharable in public.

In the future new link can be generated with the same keys if you chose to save the creation keys. To do so add the `sign` parameter to the hash. Make sure the keys are a valid key.

```
#create#sign=...##Hello%20Mars!
```

Every time you generate a new link with the same key the salt is randomised. This cause evey link to be different and can thus not easily be tracked.

To encrypt a file instead of raw data use `url`

```
#create#url##https://example.com/your/file.type
```

You will now also get a link creator. Save this link and once you uploaded the encrypted file elsewhere. add that url to the end and create the final obfuscated link. You'll also get the private link again in case you lost that one.

## 

This is a proof of concept but feel free to copy or itterate upon this work. I have made the effort to release it into the public domain.
