# combination-text


`function getTagCom(){
    const tags = new Set();
    const tagRegex = /^(Group|Category|Subcategory|Make|Mode|Diagram|Instruction)_[\w-]+$/;
    const parts = 'Group_Electric-Pallet-Jack-Parts, Category_switches,Subcategory_lgnition-Switch'.split(/[,\-\s]+/);
    
    
    for(const part of parts){
        console.log(part)
        if (tagRegex.test(part)){
            tags.add(part);
        }
    }
    console.log(tags,"tagstags")
    
    const groups = new Map();
    for(const tag of tags){
        const [group, value] = tag.split(' ');
        groups.set(groups, value);
    }
    console.log(groups,"groupsgroups")
    if(groups.size<4 || !groups.has('Group') || !groups.has('Category') || !groups.has('Subcategory') || !groups.has('Make')){
        return[];
    }
    const combination = [];
    const groupValues = groups.get('Group').split('-')
    const categoryValues = groups.get('Category').split('-')
    const subcategoryValues = groups.get('Subcategory').split('-')
    const makeValue = groups.get('Make').split('-')
        for(const groupValue of groupValue){
            console.log(groupValue, "groupValuegroupValue")
            for(const categoryValue of categoryValues){
                for(const subcategoryValue of subcategoryValues){
                    for(const makevalue of makevalues){
                       combinations.push([`Group_${groupValue}`,`Category_${categoryValue}`,`Subcategory_${subcategoryValue}`,`Make_${makevalue}`]);
                    }
                }
                
            }

        }
        return combination
        console.log(combinations,makeValue,"combinationscombinations")
}
getTagCom()

`
