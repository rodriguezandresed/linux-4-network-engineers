`mkdir -p` to create parent directories

To remove a permission for all users we can:

For example, to remove read permission, being "a" all users:

`chmod a-r test1.txt`

Or to give execute permissions to all users:

`chmod a+x test1.txt`

We can change the a for:

o -> other

g-> group

u-> user

Setting all at once:

`chmod u=rx, g-w, o-x test1.txt`

write permission on files -> you can edit them

write permission on directories -> you can create/delete directories

