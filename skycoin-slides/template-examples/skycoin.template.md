
# Skycoin Template Example

---

# H1
## H2
### H3
#### H4
##### H5
###### H6
Body text. 

---

# This is an H1 headline
## This is an H2 headline

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec vitae erat feugiat, blandit tortor nec, lobortis velit. Nunc tristique ligula ut turpis dignissim vehicula. Sed eget scelerisque nisl. Etiam consequat urna efficitur, tempor est ac, aliquet lacus. Integer imperdiet, sem a maximus porttitor, risus turpis maximus est, nec faucibus purus dui sed sem. Nunc eleifend ac lectus eget posuere. Aenean porta, ligula nec aliquam gravida.
Ut venenatis rutrum enim sit amet ultrices. Quisque fringilla egestas interdum. Aliquam vulputate dignissim accumsan. Morbi non pulvinar neque. Integer eu sodales nisi. Vivamus et leo non sapien viverra hendrerit. Aliquam erat volutpat.

---
# Code Example
```
 // SnapshotHash returns hash of UxBody + UxHead
func (uo *UxOut) SnapshotHash() cipher.SHA256 {
    b1 := encoder.Serialize(uo.Body) //body
    b2 := encoder.Serialize(uo.Head) //time, bkseq
    b3 := append(b1, b2...)
    return cipher.SumSHA256(b3)
}
```
