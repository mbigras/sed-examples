# sed-examples

> Collection useful Sed examples

## Examples

```
sed '' <<EOF
foo
bar
baz
EOF
foo
bar
baz
```

```
sed 's/foo/cats/' <<EOF
foo
bar
baz
EOF
cats
bar
baz
```

```
sed '/^b.*/d' <<EOF
foo
bar
baz
EOF
foo
```

```
sed -n '' <<EOF
foo
bar
baz
EOF
```

```
sed -n '/bar/,/baz/p' <<EOF
foo
bar
flapjacks
baz
EOF
bar
flapjacks
baz
```

```
sed -n '/bar/,/baz/ { /bar/d; /baz/d; p; }' <<EOF
foo
bar
flapjacks
baz
EOF
flapjacks
```