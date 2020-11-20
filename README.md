# rn-modal-dropdown
A react-native dropdown component for both iOS and Android.

### using

1、`npm install git+https://github.com/liukan123/rn-modal-dropdown.git#1.0.0`

2、

```
<Dropdown 
        defaultValue={this.state.patientId} 
        options={relationshipArr}
        children={(
            <View style={{height: 40, width: 50, justifyContent: 'center', alignItems: 'flex-end'}}>
                <Image style={{width: 11, height: 6}} source={require('../images/arrow_down.png')}/>
            </View>
        )}
        renderItem={(item, index, separators) => {
            return (
                <View style={{padding: 10, justifyContent: 'center', alignItems: 'center', backgroundColor: '#fff', borderBottomWidth: 1, borderBottomColor: '#F4F4F4'}}>
                    <Text style={{color: '#333', fontSize: 16, lineHeight: 18}}>{item.name}</Text>
                </View>
            )
        }}
        adjustFrame={(style) => {
            style.height -= 47;
            return style;
        }}
        onSelect={(index, item) => {
            this.setState({
                patientId: item.name,
                patientRelation: item.type,
            })
        }}/>
```



