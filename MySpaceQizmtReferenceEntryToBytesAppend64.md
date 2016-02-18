<a href='Hidden comment: Image:'></a><img src='http://qizmt.googlecode.com/svn/wiki/images/Qizmt_logo_small.png' alt='Qizmt logo (small)' />

Back to <a href='Hidden comment: Link:'></a>[Wiki Main](Main.md) / [MySpace Qizmt Reference](MySpaceQizmtReference.md) / [Static methods of Entry](MySpaceQizmtReferenceEntryStaticMethods.md)



# `ToBytesAppend64` #
`public static void ToBytesAppend64(Int64 x, List<byte> list)`

Converts int x to bytes in big endian byte ordering and appends to list.

### Example ###
```
List<byte> myBuffer = new List<byte>();

public virtual void Map(ByteSlice line, MapOutput output)
{
    string sLine = line.ToString();
    myBuffer.Clear();
    Entry.ToBytesAppend64(Convert.ToInt64(sLine), myBuffer);
    output.Add(ByteSlice.Prepare(myBuffer), ByteSlice.Prepare());
} 
```