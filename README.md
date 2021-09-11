# download-tartifact

Composite GitHub Action that solves for a shortcoming of the current [download-artifact](https://github.com/actions/download-artifact) action, in which any artifacts downloaded lose their file privileges (namely, execution privilege).

This action is to be used in conjunction with [upload-tartifact](https://github.com/alehechka/upload-tartifact) and will download the artifact and extract all files in the `artifact.tar` file. The `actions/download-artifact@v2` action is used directly to download the artifact.

> Note: The `path` provided to `upload-tartifact` will be maintained through tar, so after `download-tartifact`, any subfolder structure will remain intact.
