# docker images

images and what they have installed

## arch based

| image name | [cuda-libtorch](cuda-libtorch/Dockerfile) | [cuda](cuda/Dockerfile) | [cpp](cpp/Dockerfile) |
| ---------- |-------------------------------------------|-------------------------|-------------------------|
| base image |             archlinux:latest              |    archlinux:latest     |    archlinux:latest     |
| cmake      | ✔️                                        | ❌                     | ✔️                     |
| make       | ✔️                                        | ❌                     | ✔️                     |
| gcc        | ✔️                                        | ❌                     | ✔️                     |
| cuda       | ✔️                                        | ✔️                     | ❌                     |
| cudnn      | ✔️                                        | ✔️                     | ❌                     |
| libtorch   | ✔️                                        | ❌                     | ❌                     |
| wget       | ✔️                                        | ❌                     | ❌                     |
| unzip      | ✔️                                        | ❌                     | ❌                     |
