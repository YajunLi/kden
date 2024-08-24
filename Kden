function g = Kden(v,t,r)

  % v: N by 1, scalar data
  % t: M by 1, density to be evaluated at
  % r: scalar, param to select bandwidth, default r=-1/5
  
N = size(v,1);
M = size(t,1);
s = std(v);
h = s*N^(-r);               %  bandwidth
g = zeros(M,1);
i = 1;

    while i <= M
        z = (t(i)-v)/h;     %  N by 1
        K = normpdf(z)/h;
        g(i) = mean(K);        
        i = i + 1;
    end
end


