  def recur_fib(n)
    acc = [0, 2]
  
    f = ->(acc) {
      if acc.last() > n
         acc
      else
        cur, last = acc.last(2)
        f.(acc + [cur + last*4])
      end
    }
  
    f.(acc)
  end



  def sub
    sum = 0
    array = recur_fib(4000000)
    
    array.each do |item|
      sum += item
    end
    return sum
  end


  puts sub()