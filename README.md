# docker-volume-snapshot
Docker volume snapshot utility command

## matatata fork
preserve xattrs and acls

## Installation
```sh
sudo curl -SL https://raw.githubusercontent.com/matatata/docker-volume-snapshot/main/docker-volume-snapshot -o /usr/local/bin/docker-volume-snapshot
```
```sh
sudo chmod +x /usr/local/bin/docker-volume-snapshot
```

## Usage
```
docker-volume-snapshot (create|restore) source destination
  create         create snapshot file from docker volume
  restore        restore snapshot file to docker volume
  source         source path
  destination    destination path
```

## Example
```sh
docker-volume-snapshot create xyz_volume xyz_volume.tar
```
```sh
docker-volume-snapshot restore xyz_volume.tar xyz_volume
```

## Compression
Supports tar's compression algorithms automatically based on the file extention, for eaxmple .tar.gz
```sh
docker-volume-snapshot create xyz_volume xyz_volume.tar.gz
```
```sh
docker-volume-snapshot restore xyz_volume.tar.gz xyz_volume
```
