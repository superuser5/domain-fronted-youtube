
# Domain Fronted Youtube

Basic circumvention tool for searching and downloading from youtube, should \*.googlevideo.com and drive.google.com be unblocked. 
It can be used to bypass both tls inspection and outright blocks of the youtube domain by sending requests to 
the fronting domain (in this case drive.google.com) with the "Host: www.youtube.com" header. 
The video downloads themselves are left unobscured, as google does not support fronting for their ephemeral video 
links.

It currently supports limited search functionality and the ability to download videos given the youtube link.

## Usage:

This program can either be called directly from the command line with:

```bash
  python3 domainfrontedyoutube/__init__.py
```

Or used as a module with:

```python
  import domainfrontedyoutube
  domainfrontedyoutube.downloadfromlink(link)
```

Search functionality is only availible when importing it as a module. Video search is done with:

```python
  domainfrontedyoutube.searchyoutube(query)
```

