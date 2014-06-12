package trie

type Trie struct {
  value rune
	children []Trie
}

func (start *Trie) add (string string) bool{
	var findOrNot bool
	existed := true
	//TODO throw error if space in string
	for _,char:=range string + " "{
		findOrNot = false


		for _,node:=range start.children{
			if char == node.value{
				findOrNot = true
				break
			}
		}

		if findOrNot == false{
			existed = false
			start.children = append(start.children, Trie{char, []Trie{}})
			start = &start.children[len(start.children)-1]
		}
	}

	return existed
}

func (start *Trie) find(string string) bool{
	var findOrNot bool

	for _,char:=range string + ""{
		findOrNot = false

		for _,node:=range start.children{
			if char == node.value {
				start = &node
				findOrNot = true
				break
			}
		}

		if findOrNot == false{
			return false
		}
	}

	return true
}
