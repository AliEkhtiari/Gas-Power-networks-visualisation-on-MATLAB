# Gas-Power-networks-visualisation-on-MATLAB

clear all 
%this programme is created by ALi Ekhtiari to draw a simplified Irish gas
%network

load ('rec.mat');
load('send.mat');

send = send';
rec = rec';

    
weights = 1:28;



x = [100 -20 0 -10 -5 30 25 35 32 45 0 5 -1 30  35  31 33 -5 40 70  60  -20 -25 -10 70];
y = [70 60 0 50 10 40 45 42  48 55 40 42  42  15  20 10 12 15  40 60  65  40  45 5  70];
z=zeros(1,25); 
Irish_gas_net = digraph(send,rec,weights);


p.Marker = 's';
p.NodeColor = 'r';


%p = plot(Irish_gas_net);
%p = plot(Irish_gas_net,'EdgeColor','r','NodeColor','k','LineStyle','--');

plot(Irish_gas_net,'XData',x,'YData',y,'ZData',z, 'EdgeLabel',Irish_gas_net.Edges.Weight)

p.Marker = 's';
p.NodeColor = 'r';

view(2);





