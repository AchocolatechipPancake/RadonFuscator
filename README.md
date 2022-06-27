# RadonFuscator
Packer for native binaries.

### How does it work?
It encrypts all PE sections excluding .rsrc and .reloc of course and then adds a stub to a new section and sets the entrypoint there.
Then on runtime the stub decrypts the sections and jumps to OEP. It also has some simple anti dump and anti debug tricks which could be improved.

### Terms
- [x] You're free to use this code anywhere

### Contributing
1. Fork it
2. Create your branch (`git checkout -b my-change`)
3. Commit your changes (`git commit -am 'changed something'`)
4. Push to the branch (`git push origin my-change`)
5. Create new pull request

### Disclaimer
This protector will not work if the executable uses TLS callbacks but support for them can be added.

Based on: http://www.codereversing.com/blog/archives/95
