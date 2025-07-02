1. Set up kubectl and eksctl
--https://docs.aws.amazon.com/eks/latest/userguide/install-kubectl.html#kubectl-install-update
2. Download the kubectl binary for your cluster’s Kubernetes version from Amazon S3.
Kubernetes 1.33
3. curl -O https://s3.us-west-2.amazonaws.com/amazon-eks/1.33.0/2025-05-01/bin/linux/amd64/kubectl
4. Check the SHA-256 checksum for your downloaded binary with one of the following commands.
    sha256sum -c kubectl.sha256
5. Apply execute permissions to the binary.
    chmod +x ./kubectl
6. Copy the binary to a folder in your PATH. If you have already installed a version of kubectl, then we recommend creating a $HOME/bin/kubectl and ensuring that $HOME/bin comes first in your $PATH.
    mkdir -p $HOME/bin && cp ./kubectl $HOME/bin/kubectl && export PATH=$HOME/bin:$PATH
7. (Optional) Add the $HOME/bin path to your shell initialization file so that it is configured when you open a shell.
    echo 'export PATH=$HOME/bin:$PATH' >> ~/.bashrc

1. install eksctl
# for ARM systems, set ARCH to: `arm64`, `armv6` or `armv7`
ARCH=amd64
PLATFORM=$(uname -s)_$ARCH

curl -sLO "https://github.com/eksctl-io/eksctl/releases/latest/download/eksctl_$PLATFORM.tar.gz"

# (Optional) Verify checksum
curl -sL "https://github.com/eksctl-io/eksctl/releases/latest/download/eksctl_checksums.txt" | grep $PLATFORM | sha256sum --check

tar -xzf eksctl_$PLATFORM.tar.gz -C /tmp && rm eksctl_$PLATFORM.tar.gz

sudo install -m 0755 /tmp/eksctl /usr/local/bin && rm /tmp/eksctl