import java.util.Arrays;

//it's gonna be a generic type of array (dynamic)
public class DynamicArray<T> {
	Object data[];
	int size;
	public DynamicArray() {
		size = 0;
		data = new Object[1];
	}
	
	//get element by index
	public T get(int index) {
		return (T) data[index];
	}
	
	//add element
	public void put(int element) {
		ensureCapacity(size+1);
		data[size++] = element;
	}
	
	//ensure that there is a place for the next added element otherwise the size will be doubled
	public void ensureCapacity(int minCapacity) {
		int oldCapacity = data.length;
		if(minCapacity > oldCapacity) {
			int newCapacity = oldCapacity * 2;
			if(newCapacity<minCapacity)//case of delete the new capacity may be less than the min capacity
				newCapacity = minCapacity;
			data = Arrays.copyOf(data, newCapacity);
		}
	}
	
	public int getSize() {
		return data.length;
	}
	
}
